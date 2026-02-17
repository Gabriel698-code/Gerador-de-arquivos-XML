# 🏢 Gen System — Emissor NF-e (Web)

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

Uma aplicação web *Single-Page* desenvolvida em **Vanilla JavaScript** para preenchimento, cálculo e geração de arquivos XML de Nota Fiscal Eletrônica (NF-e v4.00) no padrão da SEFAZ brasileira. 

Este projeto foi construído para demonstrar o domínio de fundamentos do desenvolvimento web, manipulação da DOM, consumo de APIs REST e implementação de regras de negócio complexas no lado do cliente.

## 🚀 Funcionalidades Principais

* **Geração Dinâmica de XML:** Constrói a estrutura completa do XML da NF-e (v4.00) diretamente no navegador, formatando os dados de emitente, destinatário, produtos e totais.
* **Cálculo Automático:** Realiza o somatório de valores de produtos, frete e despesas acessórias em tempo real.
* **Geração de Chave de Acesso:** Algoritmo implementado em JS para gerar a chave de acesso de 44 dígitos com cálculo de Dígito Verificador (Módulo 11).
* **Consumo de API Externa:** Integração com a API do **ViaCEP** para preenchimento automático de endereço via requisição assíncrona (`fetch`).
* **UI/UX Focada no Usuário:** * Modais interativos para seleção rápida de **NCM** (Nomenclatura Comum do Mercosul), **CFOP** e Unidades de Medida.
  * Alternância dinâmica entre formulários de NF-e (Mod. 55) e NFC-e (Mod. 65), exibindo campos de segurança (CSC) apenas quando necessário.
* **Preparado para Backend:** O script já possui a estrutura `fetch` para enviar o XML gerado via método `POST` (`/salvar_nota`) para um servidor.

## 🧠 Desafios Técnicos e Aprendizados

Desenvolver um emissor de notas fiscais exige precisão. Os principais desafios resolvidos neste projeto incluem:
1. **Lógica de Validação:** Garantir que o NCM tenha exatamente 8 dígitos e o CNPJ 14 dígitos antes da submissão.
2. **String Building Seguro:** Criação de funções como `escapeXml()` para tratar caracteres especiais (`<`, `>`, `&`) e evitar quebra da estrutura do XML gerado.
3. **Gerenciamento de Estado na DOM:** Adição e remoção dinâmica de linhas na tabela de produtos, recalculando os totais gerais automaticamente a cada input do usuário.

## 🛠️ Como Executar o Projeto

Como a aplicação não depende de frameworks complexos de frontend, basta clonar o repositório e abrir o arquivo no seu navegador:

```bash
# Clone o repositório
git clone [https://github.com/Gabriel698-code/gen-system-nfe.git](https://github.com/Gabriel698-code/gen-system-nfe.git)

# Acesse a pasta do projeto
cd gen-system-nfe

# Abra o arquivo nfe_simples.html no navegador
