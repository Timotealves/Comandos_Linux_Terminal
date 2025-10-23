
---

## ⚙️ Descrição do Script Principal

### 🔍 `filtra-logs.sh`
Script criado para **varrer diretórios de logs**, procurar por palavras-chave e **remover dados sensíveis**.

#### 🧾 O que ele faz:
- Busca todos os arquivos `.log` dentro de um diretório específico.  
- Filtra linhas que contenham `"ERROR"` ou `"SENSITIVE_DATA"`.  
- Substitui informações críticas por `REDACTED`, como:
  - Senhas de usuários  
  - Tokens de sessão  
  - Chaves de API  
  - Dados de cartão  

#### 🧰 Comandos usados:
```bash
grep "ERROR" arquivo.log
sed -i 's/padrão/novo_texto/g' arquivo
find ./logs -name "*.log"
chmod 600 arquivo
mktemp /tmp/filtrado.XXXXXX
