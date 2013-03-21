* Arquivos e diretórios

corpus/           Arquivos Kern e partituras em PDF que estamos usando 
                  (sonatas de Beethoven)

corpus.txt        Lista os arquivos que estão no corpus/

ana2.py           Lê uma sonata em corpus/ e procura por intervalos
                  usados por Scarlatti

downloadsonatas.py Faz download de todas as 32 sonatas de Beethoven do
                    KernScores


== Descrição do algoritmo em ana2 ==

O programa carrega uma sonata, no momento estamos usando arquivos .krn.
Então, há a escolha de uma voz da sonata, e a obtenção de todas as notas,
somente as alturas, em sequência. Por último, são removidas todas as notas
repetidas.

Depois disso, o programa percorre a voz, começando em cada nota, para procurar
os temas/traços/motivos de interesse, levando em consideração somente a direção do movimento.
Depois de percorridas as vozes, e registradas as incidências,
as linhas são novamente percorridas para obtenção dos compassos das incidências.


== Descrição do algoritmo em ana3 ==

Igual a ana2, mas são percorridas todas as vozes de todas as sonatas.

== "Gestos" ==

=== Gesto 1: Terças paralelas nas duas mãos ===

Scarlatti K9, compasso 8
http://petrucci.mus.auth.gr/imglnks/usimg/8/86/IMSLP261887-PMLP330437-scarlatti_d_minor_k9.pdf

Beethoven op73, compasso (ver início)
http://conquest.imslp.info/files/imglnks/usimg/c/c7/IMSLP01209-Beethoven_Piano_concerto_No.5_in_Eb_Major_1stMvt.pdf

O que é: Escala com progressões de terças.

Algoritmo: Busca as direções (+1 +1 +1 ...) na voz mais aguda, com
correspondência (em direções, +1 +1 +1 ...) na voz mais grave. Com
ambas vozes tendo as mesmas durações de suas notas.

=== Gesto 2:  ===

Scarlatti K159, compasso 11
http://javanese.imslp.info/files/imglnks/usimg/6/69/IMSLP133261-WIMA.ee68-Scarlatti_Sonate_K.159.pdf

Beethoven op28 (sonata 15), 4o. movimento (pagina 16) compasso 1
http://petrucci.mus.auth.gr/imglnks/usimg/4/45/IMSLP00015-Beethoven__L.v._-_Piano_Sonata_15.pdf

Algoritmo: Em durações do tipo desce-sobe (-1 +1 -1 +1 ...), a voz que
sobe é sempre o dobro em duração da que desce.

== Motivos ==

