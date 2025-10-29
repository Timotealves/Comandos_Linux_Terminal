Funcionalidades

O script realiza as seguintes tarefas:

📁 Criação de diretórios

logs-processados: armazena logs processados e estatísticas.

logs-temp: diretório temporário para manipulação antes da compactação.

🔍 Filtragem de logs

Localiza todos os arquivos .log em logs.

Filtra linhas contendo:

"ERROR"

"SENSITIVE_DATA"

🛡️ Redação de dados sensíveis

Substitui informações críticas por REDACTED:

Senhas de usuário

Tokens de reset de senha

Chaves de API

Últimos dígitos de cartões de crédito

Tokens de sessão

📑 Organização e deduplicação

Ordena os logs filtrados.

Remove linhas duplicadas.

📊 Geração de estatísticas

Calcula:

Número de linhas

Número de palavras

Salva em log_stats_YYYY-MM-DD.txt

🖥️ Classificação por tipo de log

Prefixa linhas de logs:

[FRONTEND] para frontend

[BACKEND] para backend

Combina todos os logs em logs_combinados_YYYY-MM-DD.log.

📦 Compactação

Move arquivos processados para o diretório temporário.

Cria um arquivo .tar.gz em logs-processados.

Remove o diretório temporário automaticamente.

📂 Estrutura de Diretórios
myapp/
├─ logs/               # Logs originais
├─ logs-processados/   # Logs filtrados e arquivos compactados
└─ logs-temp/          # Diretório temporário para processamento

⚡ Como usar

Coloque seus arquivos de log em ../myapp/logs/.

Torne o script executável:

chmod +x processa_logs.sh


Execute o script:

./processa_logs.sh


Resultado:

Logs processados e estatísticas em logs-processados ✅

Arquivos temporários removidos automaticamente 🧹

Backup compactado em .tar.gz 📦

📝 Observações

🔐 Segurança: Nenhuma informação sensível será mantida nos logs finais.

🏷️ [FRONTEND] e [BACKEND] ajudam a identificar rapidamente a origem dos erros.

⚙️ Você pode ajustar os padrões de filtragem (grep e sed) conforme suas necessidades.
