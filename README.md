# Eproc Sentence Extract - ESE
 
 Script para **dividir** as sentenças do Eproc e **extrair o texto** puro (sem processamento).

 ## O script é dividido em 3 partes independentes
 
 **Parte 1**. Separação de PDFs: lê múltiplos arquivos PDFs com sentenças combinadas, geradas a partir da opção "imprimir" na busca do Eproc, e separa cada sentença individualmente.
 
 **Parte 2**. Extração de texto: com as sentenças separadas por arquivo PDF (geradas em 1), extrai o texto de cada PDF e cria um arquivo TXT (texto puro) com o conteúdo textual de cada sentença.

 **Parte 3**. Renomeação dos arquivos numericamente: renomeia os arquivos TXT para uma sequência numérica a partir de determinado número inicial (variável 'start_number').

## Dependências
Para o script ser executado é necessário instalar a biblioteca PyPDF2 (dependência).
> `pip install PyPDF2` (primeira célula do notebook).

Há uma possibilidade de utilizar a biblioteca `spaCy` para dividir as 'frases' das sentenças e gerar conteúdo do TXT com melhor divisão das frases.
Porém, o código está comentado, pois o resultado não foi muito vantajoso.

Se a biblioteca `spaCy` for utilizada, é necessário instalar a biblioteca e o pacote de idioma para português.
> `pip install -U spacy` # Biblioteca

> `python -m spacy download pt` # Pacote de idioma para português

OBS1: no código original, o uso da biblioteca spaCy é opcional e está comentado (desativado). Ou seja, essa dependência não é obrigatória!

OBS2: o divisor de "frases" da NLTK não foi testado.

## Detalhes

1. Os PDFs gerados na opção "Imprimir" da busca do Eproc devem ser colocados na pasta "input" para o processamento da Parte 1.
2. O nome dos arquivos PDFs gerados na Parte 1 são os números dos processos extraídos de cada sentença.
3. Os arquivos resultantes da Parte 1 serão gerados na pasta 'output'. A pasta 'output' será utilizada como entrada e saída da Parte 2. Isso porque as sentenças individualizadas, uma em cada PDF, que são geradas na pasta 'output' serão lidas dessa pasta e os arquivos TXT serão gerados e escritos nessa mesma pasta com o mesmo nome (número do processo) para que os arquivos sejam facilmente associados.
4. Para a Parte 3, os arquivos TXT devem ser colocados na pasta `sentences_txt`.


## Autor

Código feito em 06/06/2024 por [Eduardo Alves da Silva](https://github.com/edualvss).
