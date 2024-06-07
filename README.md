# Eproc Sentence Extract
 
 Script para dividir as sentenças do Eproc e extrair o texto.

 O script é dividido em 2 partes independentes:
 
 **Parte 1**. Separação de PDFs: lê múltiplos arquivos com sentenças combinadas, geradas a partir da opção "imprimir" na busca do Eproc, e separa cada sentença individualmente.
 
 **Parte 2**. Extração de texto: com as sentenças separadas por arquivo (geradas em 1), extrai o texto de cada PDF e cria um arquivo TXT (texto puro) com o conteúdo textual de cada sentença.

Para o script ser executado é necessário instalar a biblioteca PyPDF2 (dependência) `pip install PyPDF2` (primeira célula do notebook).

Os PDFs gerados na opção "Imprimir" da busca do Eproc devem ser colocados na pasta "input" para o processamento da Parte 1.
O nome dos arquivos PDFs gerados na Parte 1 são os números dos processos extraídos de cada sentença.

Os arquivos resultantes da Parte 1 serão gerados na pasta 'output'. A pasta 'output' será utilizada como entrada e saída da Parte 2. Isso porque as sentenças individualizadas, uma em cada PDF, que estão na pasta 'output' serão lidas dessa pasta e os arquivos TXT serão gerados e escritos nessa mesma pasta.


