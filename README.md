# Projeto de Integração de Sistemas de Informação

Este projeto foi desenvolvido como parte da disciplina de **Integração de Sistemas de Informação (ISI)**, focando na aplicação e experimentação de ferramentas de **ETL (Extract, Transform, Load)** utilizando o **Pentaho Kettle (PDI)**.

## Autor

- **Alexandre Mykyta**  
- Nº **27998**

## Estrutura do Projeto

O projeto está organizado da seguinte forma:

- **doc/**: Contém o relatório do trabalho, que documenta todo o desenvolvimento e os resultados obtidos.
  
- **data/output/**: Inclui os ficheiros gerados durante o processo de transformação, que são:
  - `Student.html`: Resultado da transformação do XML para HTML.
  - `Student.json`: Dados transformados em formato JSON.
  - `Student.xlsx`: Dados transformados em formato Excel.
  - `Student.txt`: Dados transformados em formato TXT.

- **data/input/**: Contém o ficheiro `Student.xsl`, que é utilizado para a transformação de XML para HTML.

- **dataint/**: Inclui o job e as transformações desenvolvidas no Pentaho Kettle, que gerenciam todo o processo de ETL. As transformações incluem:
  - **GetStudentInfo**: Realiza a obtenção dos dados do JSON e os armazena.
  - **htmlAsAmbient**: Concatena todo o HTML em uma única string.
  - **JobStudent**: Envia o email com o conteúdo gerado.

## Funcionamento

O projeto realiza a seguinte sequência de operações:

1. **Aquisição de Dados**: O projeto inicia-se com a obtenção de um ficheiro JSON da internet contendo os dados dos alunos e respetivas notas.  
2. **Tratamento e Transformação**: Os dados são tratados e convertidos para os formatos XML, Excel, TXT e JSON.  
3. **Transformação de XML para HTML**: Utiliza-se o ficheiro XSL (`Student.xsl`) para transformar o XML gerado num ficheiro HTML formatado.  
4. **Envio de Resultados**: Os resultados são processados e enviados como parte do corpo de uma mensagem de email.

## Requisitos

- Ferramenta de ETL: **Pentaho Data Integration (Kettle)**
- Acesso à internet para a obtenção dos dados JSON
- Java Runtime Environment (JRE)

## Conclusão

Este projeto demonstrou a eficácia das ferramentas de ETL na integração de sistemas de informação, destacando a importância da normalização, transformação e envio automatizado de dados através de diferentes formatos.



