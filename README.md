# Sistema de Geração de Propostas Personalizadas

Este é um aplicativo web desenvolvido em Python usando Streamlit que permite gerar propostas personalizadas em PDF a partir de um template PowerPoint.

## Requisitos do Sistema

### Windows
- Python 3.x
- LibreOffice (versão 7.0 ou superior)
- Git (opcional, para clonar o repositório)

### macOS
- Python 3.x
- LibreOffice (versão 7.0 ou superior)
- Git (opcional, para clonar o repositório)
- Homebrew (para instalar o LibreOffice)

### Linux
- Python 3.x
- LibreOffice (versão 7.0 ou superior)
- Git (opcional, para clonar o repositório)

## Instalação

### 1. Instalação do LibreOffice

#### Windows
1. Baixe o instalador do LibreOffice em: https://www.libreoffice.org/download/download/
2. Execute o instalador e siga as instruções
3. Adicione o LibreOffice ao PATH do sistema (geralmente em `C:\Program Files\LibreOffice\program`)

#### macOS
```bash
# Instale o Homebrew se ainda não tiver
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Instale o LibreOffice
brew install libreoffice
```

#### Linux (Ubuntu/Debian)
```bash
sudo apt update
sudo apt install libreoffice
```

### 2. Instalação do Python e Dependências

1. Clone este repositório (ou baixe os arquivos):
```bash
git clone [URL_DO_REPOSITÓRIO]
cd projeto_baterias
```

2. Crie um ambiente virtual (recomendado):
```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

3. Instale as dependências:
```bash
pip install -r requirements.txt
```

## Estrutura de Arquivos

- `main.py`: Aplicação principal Streamlit
- `relacao_empresas_cargas.csv`: Arquivo CSV com dados de clientes e cargas
- `template_propostas.pptx`: Template PowerPoint para as propostas
- `requirements.txt`: Lista de dependências do projeto

## Como Usar

1. Execute a aplicação:
```bash
streamlit run main.py
```

2. No navegador:
   - Selecione o Nome do Cliente no primeiro dropdown
   - Selecione a Carga correspondente no segundo dropdown
   - Clique em "Gerar Proposta" para criar o PDF

## Funcionalidades

- Seleção dinâmica de clientes e cargas
- Filtragem automática de cargas por cliente
- Geração de PDF personalizado a partir de template PowerPoint
- Download automático do PDF gerado

## Solução de Problemas

### Problemas comuns e soluções:

1. **Erro ao carregar o LibreOffice**
   - Verifique se o LibreOffice está instalado corretamente
   - No Windows, verifique se o caminho do LibreOffice está no PATH do sistema
   - No macOS/Linux, tente executar `soffice --version` no terminal para verificar a instalação

2. **Erro ao gerar PDF**
   - Verifique se o arquivo template existe e está no formato correto
   - Verifique se o template contém os placeholders `{{NOME_CLIENTE}}` e `{{NOME_CARGA}}`
   - Verifique as permissões do diretório temporário

3. **Erro ao carregar o CSV**
   - Verifique se o arquivo CSV está no formato correto (separador ponto e vírgula)
   - Verifique se as colunas estão nomeadas corretamente: "NOME EMPRESARIAL" e "NOME CARGA"

## Suporte

Para suporte ou dúvidas, abra uma issue no repositório do projeto ou entre em contato com a equipe de desenvolvimento. 