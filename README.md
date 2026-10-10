# SyncFolder — atualizações

Repositório público usado pelo atualizador do SyncFolder para distribuir instaladores e metadados das versões. O código-fonte e os arquivos internos do projeto devem permanecer em um repositório privado separado.

## Arquivos de cada Release

Anexe somente os arquivos produzidos pelo mesmo build:

- `SyncFolder-Setup-<versão>.exe`;
- `latest.yml`;
- o arquivo `.blockmap`, quando produzido pelo build.

Não anexe ZIPs do projeto, arquivos de ambiente, chaves privadas, tokens, bancos de dados, backups ou logs de usuários. Credenciais administrativas e credenciais das integrações pertencem ao servidor e não devem ser incluídas no instalador.

## Publicação protegida

As próximas Releases usam imutabilidade: os anexos ficam bloqueados para alteração depois da publicação.

1. Crie a Release como **rascunho**, com uma nova tag de versão.
2. Anexe todos os arquivos e confira a versão e os nomes referenciados por `latest.yml`.
3. Publique somente depois de conferir os anexos completos.
4. Atualize a versão mínima exigida pelo aplicativo somente depois de confirmar que a Release está disponível e pode ser baixada.

Corrija um instalador publicado lançando uma nova versão. Não reutilize tags nem substitua anexos de uma versão já publicada.

## Proteção dos commits

O `.gitignore` limita os arquivos adicionados normalmente ao Git à documentação e à configuração do repositório. Ele reduz inclusões acidentais e não substitui a revisão dos arquivos nem a detecção de segredos do GitHub. As regras preservam o histórico da branch principal e as tags `v*`, permitindo commits normais e novas versões.
