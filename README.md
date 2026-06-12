# 📝 Tratamento de Dados Cadastrais com Python (openpyxl)

Este script em Python automatiza a limpeza e o tratamento de dados em planilhas do Excel (`.xlsx`). Ele foi desenvolvido especificamente para padronizar colunas de identificação, removendo prefixos indesejados de forma rápida e eficiente.

## 🚀 Funcionalidades

O script realiza a leitura de uma planilha existente e faz as seguintes limpezas linha por linha:

* **Coluna 1 (`CodAluno`):** Identifica se o código começa com a letra **"M"** (maiúscula ou minúscula) e remove esse caractere, mantendo apenas o restante do texto/número.
* **Coluna 3 (`NumCartao`):** Realiza a mesma validação e limpeza, removendo o prefixo **"M"** caso ele exista.
* **Exportação Segura:** Salva os dados tratados em um novo arquivo, preservando a planilha original intacta.

---

## 🛠️ Pré-requisitos

Antes de executar o script, você precisará ter o Python instalado e a biblioteca `openpyxl` (utilizada para manipular arquivos do Excel).

Você pode instalar a dependência necessária rodando o seguinte comando no seu terminal:

```bash
pip install openpyxl

```

---

## 💻 Como Usar

1. Baixe ou copie o script para a pasta do seu projeto.
2. Certifique-se de que a planilha que você deseja tratar está na mesma pasta (ou ajuste o caminho no código).
3. Abra o script e configure os nomes dos arquivos nas variáveis iniciais:
```python
nome_arquivo_original = "seu_arquivo.xlsx"  # Nome do arquivo de entrada
nome_arquivo_salvar = "seu_arquivo_tratado.xlsx"  # Nome do arquivo de saída

```


4. Execute o script:
```bash
python nome_do_seu_script.py

```



---

## 📊 Exemplo Prático de Funcionamento

**Antes do tratamento (Planilha Original):**

| CodAluno (Col 1) | Nome | NumCartao (Col 3) |
| --- | --- | --- |
| **M**12345 | João Silva | **M**98765 |
| 54321 | Maria Souza | 56789 |
| **m**99999 | Pedro Santos | **M**11111 |

**Depois do tratamento (Planilha Tratada):**

| CodAluno (Col 1) | Nome | NumCartao (Col 3) |
| --- | --- | --- |
| **12345** | João Silva | **98765** |
| 54321 | Maria Souza | 56789 |
| **99999** | Pedro Santos | **11111** |

---

## ⚠️ Observações importantes

> 📌 **Nota:** O script pressupõe que a **linha 1** contém os cabeçalhos da tabela, portanto a varredura e alteração dos dados começam estritamente a partir da **linha 2**.
