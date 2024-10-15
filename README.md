# Deploy de CS-Icorp Tabelas

**Author:** Agnaldo Barros e Valter Gabriel  
**Data:** 15.10.2024  

## Objetivo

Efetuar as publicações nos diversos containers de homologação e produção.

O objetivo principal é efetuar o deploy do produto **CS-Icorp Tabelas** nos ambientes de homologação e produção. Os ambientes de produção são diversos, como `app1`, `app3`, `app4`, etc. Cada ambiente tem uma **URL base** diferente. Exemplo:

- `https://app1.csicorpnet.com.br`
- `https://app3.csicorpnet.com.br`
- `https://app4.csicorpnet.com.br`

## Identificação dos Ambientes

Para atender esse requisito, o ambiente a ser utilizado será passado como parâmetro (ex: `dev`, `prod`). Esses identificadores serão responsáveis por rotear a URL base de acordo com o ambiente desejado. O mapeamento atual dos ambientes e URLs é o seguinte:

- **dev**  
  URL Base: `https://dsv17.csicorpnet.com.br`  
  Executando no container: `teste1.csicorpnet.com.br`

- **prod_app1**  
  URL Base: `https://app1.csicorpnet.com.br`  
  Executando no container: `teste2.csicorpnet.com.br`

- **prod_app3**  
  URL Base: `https://app3.csicorpnet.com.br`  
  Executando no container: `teste3.csicorpnet.com.br`

- **prod_app4**  
  URL Base: `https://app4.csicorpnet.com.br`

## Processo de Deploy

A versão a ser fornecida deve corresponder ao valor de versão do projeto. O processo de geração via YAML segue a seguinte sequência:

1. **Gerar a pasta do projeto** e copiar os arquivos para ela.
2. **Gerar os submódulos** e transferir os arquivos deles para as respectivas pastas do projeto.
3. **Gerar a imagem** e o container.

### Nomenclatura

- **Imagem:** `csim-tabelas_${ambiente}_${{versao}}`
- **Container:** `csct-tabelas_${ambiente}_${{versao}}`
