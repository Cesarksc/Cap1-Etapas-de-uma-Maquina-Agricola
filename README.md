
# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
<a href="https://www.fiap.com.br/"><img src="assets/logo-fiap.png" alt="FIAP - Faculdade de Informática e Admnistração Paulista" border="0" width=40% height=40%></a>
</p>

<br>

# Agro Cana Perdas

## Grupo: [Nome do grupo]

## 👨‍🎓 Integrantes:
- Cesar Kayque de Sousa Carvalho - RM556399

## 📜 Descrição

Análise de Dados de Colheita de Cana-de-açúcar (Fase 3). Este projeto analisa dados da tabela `SENSORES` do Oracle para entender padrões de produção e perdas em diferentes tipos de colheita. Inclui visualizações exploratórias e modelagem preditiva com 5 algoritmos de machine learning para prever perdas financeiras.

## 📁 Estrutura de pastas

Dentre os arquivos e pastas presentes na raiz do projeto, definem-se:

- **src**: contém o notebook Jupyter principal (`CesarCarvalho_RM556399_fase3_cap1.ipynb`) com a análise completa.
- **assets**: arquivos de recursos (imagens, logos, etc).
- **.env.example**: exemplo de arquivo de variáveis de ambiente para conexão com Oracle.
- **README.md**: guia e explicação geral sobre o projeto.

## 🔧 Como executar o código

Pré-requisitos:
- Python 3.10+
- Oracle com dados na tabela `SENSORES` (opcional, notebook funciona sem conexão)
- IDE recomendada: VS Code com extensão Jupyter

Instalação:
```cmd
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
```

Depois, abra o arquivo `src/CesarCarvalho_RM556399_fase3_cap1.ipynb` no VS Code e execute as células sequencialmente.

## 🗃 Histórico de lançamentos

* 0.1.0 - 10/2025
    * Versão inicial

## 📋 Licença

<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1"><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1"><p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://github.com/agodoi/template">MODELO GIT FIAP</a> por <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://fiap.com.br">Fiap</a> está licenciado sobre <a href="http://creativecommons.org/licenses/by/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">Attribution 4.0 International</a>.</p>

## Lógica da solução

O notebook segue a seguinte estrutura:

1. **Conexão com Oracle**: Carrega dados da tabela `SENSORES` e trata erros de conexão graciosamente.
2. **Preparação de Dados**: Converte tipos de dados, normaliza valores numéricos e detecta dados ausentes.
3. **Análise Exploratória**: Visualiza distribuições de produtividade, perdas e relações entre variáveis.
4. **Análise de Perfis**: Identifica os 3 tipos de colheita mais frequentes e melhor desempenho por cenário.
5. **Modelagem Preditiva**: Treina 5 modelos (Regressão Linear, Árvore de Decisão, Random Forest, Gradient Boosting, KNN) para prever perdas financeiras.
6. **Comparação de Modelos**: Avalia MAE, RMSE e R² para identificar o melhor modelo.

## Observações
- O notebook requer uma conexão Oracle com dados pré-carregados na tabela `SENSORES`.
- Se **Oracle não estiver disponível**, a primeira célula exibirá um erro, mas você pode continuar com dados de exemplo.
- As análises usam as colunas: `AREA_HA`, `PROD_T_HA`, `PRECO_R_T`, `PERDA_PCT`, `PERDA_TON`, `PERDA_REAIS`, `TIPO_COLHEITA`, `CENARIO`.
- Configure o arquivo `.env` com suas credenciais Oracle antes de executar.

## Exemplo rápido (com Oracle)
1. Configure o arquivo `.env` com suas credenciais
2. Abra o notebook no VS Code
3. Execute a primeira célula para conectar ao Oracle
4. Execute sequencialmente as demais células para visualizar:
   - Estatísticas dos dados
   - Gráficos de distribuição e correlações
   - Análise dos 3 tipos de colheita principais
   - Treinamento e comparação dos 5 modelos preditivos
