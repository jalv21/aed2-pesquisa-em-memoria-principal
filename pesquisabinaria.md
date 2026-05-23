# 🔍 Pesquisa em Memória Principal

## Pesquisa Sequencial

Pesquisa iterativa sobre o conjunto até achar a chave de pesquisa

**Pior caso:** $$ O(n) $$
**Melhor caso:** $$ O(1) $$

## Pesquisa Binária

- Recursiva
- Funciona somente se os elementos estiverem ordenados

### Pesquisa Binária - Pseudo código
```java
se inicio > fim // todos os elementos foram descartados
    fim da pesquisa // 1º caso base
se chave de pesquisa == chave do registro do meio
    fim da pesquisa // 2º caso base
se chave da pesquisa > chave do registro do meio
    buscar do (meio + 1) até o fim;
se chave de pesquisa < chave do registro do meio
    buscar do início até (meio - 1);
```

**Pior caso**: 
$$ O(log (n)) $$

### Pesquisa Binária - Considerações

Inserir/Remover novo elemento em posições além da última precisa deslocar elementos de posição
- pior caso: *n* movimentações para inserir o elemento na posição correta

**Pesquisa binária não é ideal para aplicações com muitas inserções/remoções.**

## Comparação

Aumentando-se `n` gradativamente:
- Pesquisa sequencial cresce em escala linear
- Pesquisa binária cresce em escala logaritimica