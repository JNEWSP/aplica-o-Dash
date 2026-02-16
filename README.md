# README - Dashboard de Análise de E-commerce

## 📊 Sobre o Projeto

Este projeto consiste em um dashboard interativo desenvolvido com **Dash** (Python) para análise de dados de e-commerce. O dashboard permite visualizar métricas importantes como distribuição de preços, notas dos produtos, análise por gênero e principais marcas.

## 🚀 Funcionalidades

- **Distribuição de Preços**: Histograma mostrando a faixa de preços dos produtos
- **Distribuição de Notas**: Visualização das avaliações dos clientes
- **Preço por Gênero**: Boxplot comparando preços entre categorias (Masculino, Feminino, etc.)
- **Top 10 Marcas**: Gráfico de barras com as marcas mais frequentes

## 📁 Estrutura do Projeto

```
├── ecommerce_estatistica.csv     # Base de dados
├── dashboard_ecommerce.py         # Código principal do dashboard
└── README.md                      # Documentação
```

## 🛠️ Tecnologias Utilizadas

- **Python 3.8+**
- **Dash** - Framework para criação de dashboards
- **Plotly** - Biblioteca para visualização de dados
- **Pandas** - Manipulação e análise de dados
- **Google Colab** - Ambiente de execução (opcional)

## 📋 Pré-requisitos

```
dash
plotly
pandas
```

## 🔧 Instalação e Execução

### Opção 1: Google Colab (Recomendado)

1. Abra o [Google Colab](https://colab.research.google.com)
2. Crie um novo notebook
3. Cole o código do dashboard
4. Execute as células
5. Faça o upload do arquivo `ecommerce_estatistica.csv` quando solicitado
6. O dashboard será aberto automaticamente na própria interface do Colab

### Opção 2: Execução Local

```bash
# Clone o repositório
git clone [url-do-seu-repositorio]

# Instale as dependências
pip install dash plotly pandas

# Execute o dashboard
python dashboard_ecommerce.py
```

Acesse: `http://localhost:8050`

## 📊 Visualização dos Dados

O dashboard apresenta 4 gráficos principais:

1. **💰 Distribuição de Preços**: Analisa a variação de preços dos produtos
2. **⭐ Distribuição das Notas**: Mostra a satisfação dos clientes
3. **👕 Preço por Gênero**: Compara preços entre diferentes públicos-alvo
4. **🏆 Top 10 Marcas**: Identifica as marcas com mais produtos no catálogo

## 📈 Exemplo de Uso

```python
# Trecho do código principal
app.layout = html.Div([
    html.H1('Dashboard E-commerce'),
    dcc.Graph(figure=px.histogram(df, x='Preço', title='Distribuição de Preços')),
    dcc.Graph(figure=px.histogram(df, x='Nota', title='Distribuição das Notas')),
    dcc.Graph(figure=px.box(df, x='Gênero', y='Preço', title='Preço por Gênero')),
    dcc.Graph(figure=px.bar(df['Marca'].value_counts().head(10).reset_index(), 
                           x='Marca', y='count', title='Top 10 Marcas'))
])
```

## 🤝 Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para:

- Reportar bugs
- Sugerir novas funcionalidades
- Melhorar a documentação
- Adicionar mais visualizações

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## ✨ Autor

Desenvolvido como projeto final da disciplina de Estatística para Análise de Dados de E-commerce.

---

**Nota**: Certifique-se de ter o arquivo `ecommerce_estatistica.csv` no mesmo diretório do script ou faça o upload quando executar no Google Colab.
