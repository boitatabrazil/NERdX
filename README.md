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


## Configuração do ambiente

Antes de prosseguir com o nosso tutorial é necessário ter um ambiente de desenvolvimento preparado para as nossas necessidades. Por sorte praticamente todas as aplicações de Machine Learning em python usam o Jupyter Notebook (antigo IPython Notebook), o que torna a resolução de problemas mais tranquila devido a gigantesca comunidade e torna o ambiente mais versátil. Jupyter Notebook também oferece suporte para as linguagens R e Julia.

### Instalação

+ Python 3.7

Antes de instalar verifique se já está instalado (as últimas versões do Ubuntu já vem com python3)

		python3 --version

Se o output for algo do tipo:

		Python 3.7.3

Massa, você pode pular essa parte. (python 3.6 ou 3.8 não devem ter nenhum problema de compatibilidade com esse tutorial)

Caso não tenha python3 instalado execute os seguintes comandos

		sudo apt update
		sudo apt install software-properties-common

		sudo add-apt-repository ppa:deadsnakes/ppa

		sudo apt update
		sudo apt install python3.7

Pronto! Lembrando que se o python 3.6 já estiver instalado não é necessário fazer o update.

Lembrando que se você instalou o python 3.7 seguindo esses comandos para usar ele no terminal é necessário usar o comando python3.7 ao invés de python3 ou python

+ Pip

Pip é o gerenciador de pacotes do python.

Verifique se ele está instalado com:

		pip3 --version

Se retornar um erro instale com:

		sudo apt install python3-pip

+ Packages básicos

Usando pip instale os pacotes básicos para Machine Learning

		pip3 install pandas
		pip3 install numpy
		pip3 install nltk
		pip3 install sklearn
		pip3 install matplotlib
		pip3 install tqdm

No decorrer do tutorial irão aparecer outros pacotes.

+ Jupyter Notebook

Para instalar:

		python3 -m pip install --upgrade pip
		python3 -m pip install jupyter

https://jupyter.org/install

Para subir nosso ambiente execute o seguinte comando:

		jupyter notebook

Pronto! O jupyter vai abrir uma página no seu navegador padrão, navegue nela até a pasta code desse repositório e abra o arquivo correspondente a próxima parte deste tutorial

