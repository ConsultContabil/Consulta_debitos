# Consulta Débitos - Sistema de Extração de Débitos Fiscais

## 📋 Descrição

O **Consulta Débitos** é uma aplicação web desenvolvida em Python/Flask que automatiza a extração e análise de débitos fiscais a partir de relatórios PDF da Receita Federal. A aplicação permite que usuários façam upload de relatórios fiscais e obtenham automaticamente um resumo organizado dos débitos encontrados, incluindo valores totais e detalhamento por tipo de débito.

## ✨ Funcionalidades

- **Upload de PDF**: Interface simples para upload de relatórios fiscais em PDF
- **Extração Automática**: Análise automática do conteúdo do PDF usando regex
- **Identificação de Empresa**: Extração automática do CNPJ e nome da empresa
- **Categorização de Débitos**: Identificação e agrupamento de diferentes tipos de débitos fiscais
- **Cálculo de Totais**: Soma automática de todos os débitos encontrados
- **Interface Responsiva**: Design moderno e responsivo para diferentes dispositivos
- **Formatação Brasileira**: Valores formatados no padrão brasileiro (vírgula como separador decimal)

## 🛠️ Tecnologias Utilizadas

- **Backend**: Python 3.11.3, Flask 2.3.2
- **Processamento de PDF**: pdfplumber 0.9.0
- **Interface**: HTML5, CSS3
- **Deploy**: Heroku (Procfile, runtime.txt)
- **Servidor**: Gunicorn/Waitress

## 📦 Dependências Principais

- `Flask==2.3.2` - Framework web
- `pdfplumber==0.9.0` - Extração de texto de PDFs
- `tabulate==0.9.0` - Formatação de tabelas
- `gunicorn==20.0.4` - Servidor WSGI para produção

## 🚀 Instalação e Configuração

### Pré-requisitos

- Python 3.11.3 ou superior
- pip (gerenciador de pacotes Python)

### Passos para Instalação

1. **Clone o repositório**

   ```bash
   git clone <url-do-repositorio>
   cd Consulta_debitos
   ```

2. **Crie um ambiente virtual (recomendado)**

   ```bash
   python -m venv venv
   source venv/bin/activate  # No Windows: venv\Scripts\activate
   ```

3. **Instale as dependências**

   ```bash
   pip install -r requirements.txt
   ```

4. **Execute a aplicação**

   ```bash
   python app.py
   ```

5. **Acesse a aplicação**
   - Abra seu navegador e vá para `http://localhost:5000`

## 📖 Como Usar

1. **Acesse a aplicação** no navegador
2. **Faça upload** do arquivo PDF do relatório fiscal
3. **Clique em "Extrair Débitos"**
4. **Visualize os resultados**:
   - Nome da empresa
   - CNPJ
   - Lista detalhada de débitos por categoria
   - Valor total dos débitos

## 🏗️ Estrutura do Projeto

```
Consulta_debitos/
├── app.py                 # Aplicação principal Flask
├── requirements.txt       # Dependências Python
├── Procfile              # Configuração para deploy no Heroku
├── runtime.txt           # Versão do Python
├── static/               # Arquivos estáticos
│   ├── styles.css        # Estilos da página inicial
│   ├── styles_result.css # Estilos da página de resultado
│   ├── color.png         # Logo/ícone
│   └── download.ico      # Ícone de download
├── templates/            # Templates HTML
│   ├── index.html        # Página inicial
│   └── resultado.html    # Página de resultados
└── upload/               # Diretório para arquivos enviados
```

## 🔧 Funcionalidades Técnicas

### Extração de Dados

- **CNPJ**: Extração automática usando regex
- **Nome da Empresa**: Identificação a partir do cabeçalho do PDF
- **Débitos**: Reconhecimento de múltiplos padrões de débitos fiscais

### Padrões de Débitos Suportados

- Débitos por período (YYYY-MM)
- SIMPLES NACIONAL
- Débitos por trimestre
- Outros formatos específicos da Receita Federal

### Formatação

- Valores formatados no padrão brasileiro
- Tabelas organizadas e responsivas
- Interface intuitiva e moderna

## 🌐 Deploy

### Heroku

A aplicação está configurada para deploy no Heroku:

1. **Procfile**: Configurado para usar Waitress
2. **runtime.txt**: Especifica Python 3.11.3
3. **requirements.txt**: Lista todas as dependências

### Deploy Local

```bash
python app.py
```

## 🔒 Segurança

- Validação de tipos de arquivo (apenas PDF)
- Processamento seguro de uploads
- Sanitização de dados extraídos

## 🤝 Contribuição

Para contribuir com o projeto:

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
3. Commit suas mudanças (`git commit -am 'Adiciona nova funcionalidade'`)
4. Push para a branch (`git push origin feature/nova-funcionalidade`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.

## 👥 Desenvolvimento

Desenvolvido para automatizar o processo de análise de relatórios fiscais, reduzindo o tempo manual necessário para extrair informações de débitos da Receita Federal.

## 📞 Suporte

Para suporte ou dúvidas, entre em contato através do site: [consultcontabil.com](https://consultcontabil.com/)

---

**Desenvolvido com ❤️ para Consult Contábil**
