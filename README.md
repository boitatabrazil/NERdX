# NERdX

Pipeline de Ner do Boitatá.

Essa pipeline/tutorial tem o objetivo de apresentar técnicas básicas de NLP/PLN focando no problema de NER.

Mais informações sobre NER e o uso de Deep Learning em NLP leia nosso artigo: http://comissoes.sbc.org.br/ce-pln/stil2019/proceedings-stil-2019-Final-Publicacao.pdf (pag 404)

Nesse tutorial iremos usar o livro Jardim Noia.

Ele e outros livros estão disponíveis na pasta PDF


# Parte 1: Tratamento do Texto

Como os arquivos do texto não estão em um formato onde técnicas de NLP podem ser aplicadas, devemos tratar esse texto até o ponto em que ele fique legível para a máquina

## Pdf para txt

Nossos arquivo estão em pdf, o que não é bom pois não podemos fazer alterações no arquivo. iremos transformar ele em um arquivo txt, que nos dará a liberdade de fazer alterações no texto independente da plataforma utilizada.

Para transformar nosso pdf em txt:
+ Abra o terminal na pasta raiz desse repositorio

+ Execute os seguinte comandos:

		pip install pdfminer

		pdf2txt.py -o TXT/[NOME_DO_ARQUIVO_DE_SAIDA].txt PDF/[NOME_DO_LIVRO].pdf

			ex:  pdf2txt.py -o TXT/jardim.txt PDF/JARDIMNOIA.pdf

Pronto! Agora temos um txt onde podemos começar a trabalhar

## Tratamento do Arquivo:


Quando fizemos a operação para gerar o txt todos os ruídos do pdf foram para o txt. Devemos então remover tais ruídos.

Como a natureza desses ruídos é complicada é melhor que essa operação seja feita manualmente.

+ Abra o arquivo txt em qualquer editor de texto e remova tudo que não é parte do texto. (ex: numero de pagina, Titulo de capitulo, nota de rodapé)



