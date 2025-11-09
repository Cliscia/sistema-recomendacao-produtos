# Sistema de Recomendação de Produtos (TF-IDF + Similaridade do Cosseno)

Projeto de NLP clássico que recomenda produtos por **similaridade de texto** e por **intenção do usuário**.
Duas modalidades:
- **Baseada em item**: “produtos similares a _Airfryer_”
- **Baseada em intenção**: “quero presente útil para quem gosta de cozinhar”

## Tecnologias
- Python, Pandas, NumPy  
- scikit-learn (TfidfVectorizer, cosine_similarity)  
- Jupyter / JupyterLab

## Como funciona
1. **Feature engineering**: concatena nome, categoria, material, marca, tags, preço e nota em um texto único.
2. **TF-IDF**: transforma texto em vetores.
3. **Similaridade do cosseno**: encontra itens mais próximos.
4. **Retorno**: top-N recomendações com ID, Produto, Categoria, Preço e Avaliação.

## Uso (exemplos de código)

```python
# similares a um produto
res1 = recomendar("Airfryer")
mostrar_recomendacao_clean(res1, "Recomendações — similares a: Airfryer")

# por intenção do usuário
res2 = recomendar_por_descricao("quero presente útil para quem gosta de cozinhar")
mostrar_recomendacao_clean(res2, "Recomendações — intenção: presente útil para quem cozinha")
```



