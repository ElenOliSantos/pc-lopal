# pc-lopal
Repositório para armazenar os códigos da aula.

1. O que significa cada um dos três números?

Versão maior (X- Major):
Atualização drástica que pode renomear, remover funções antigas. Tecnicamente, mudanças incompatíveis com a versão antiga.

Versão (Y - Minor):
Novos recursos adicionados ao código. 

Versão (Z - Patch): 
Correção de pequenos erros. Não muda o código, apenas corrige "certos" bugs.


2. Quem decide como esse número muda e com base em quê?

Quem decide?
Os criadores 

Com base em quê?
Depende do impacto da mudança ao código. Exemplo: Se o criador quer apenas corrigir um bug, deve fazer uma atualização "patch". Caso ele queira fazer pequenas mudanças como, adicionar um nova função, mude para atualização "minor".Entretanto, se ele quer mudar um código, mas mude a forma como os "usuários" chamem o código, deve ser a atualização "major". 


### 1. Qual a diferença entre os dois grupos?

* **Dependencies** (Dependências de Produção):
	- O que é? Bibliotecas essenciais para que funcione para o usuário final (cliente).
	- Onde roda? No servidor de produção e no ambiente de desenvolvimento.

* **DevDependencies** (Dependências de desenvolvimento):
	- O que é? Ferramentas que ajudam na produção do código.
	- Onde roda? No computador do desenvolvedor. O usuário final (cliente) não precisa dela para usar o sistema.


### 2. Como decidir em qual grupo colocar uma biblioteca? 

- Caso instale uma biblioteca, e ela seja necessária para o usuário final conseguir rodar o código, deve ser usado a ``Dependencies``. Se não é, instale no ``DevDependencies``.


# Desafio 3 - Os símlobos de versão (^,~ e sem símbolo)

### 1. O que cada símbolo permite atualizar?

- Circunflexo (^):
	- O que permite? Atualiza nas versões ``minor``, ``patch`` mas não ``major``.
	- Como funciona? O circunflexo (^) permite que você receba correções de bugs e novas funções sem quebrar o projeto com mudanças incompatíveis.

- Til (~):
	-O que permite? Atualiza apenas versões ``patch``.
	-Como funciona? Varia apenas a última versão, fazendo com que receba apenas correção de bugs.

- Sem** símbolo:**
	- O que permite: Nenhuma atualização.
	- Como funcionar: Instala a versão especificada. 



# Desafio 4 - ``CommonJS`` vs ``ES Modules``

### 1. Como cada um surgiu?
- ``CommonJS``: 
Surgiu em 2009, com a criação do node.js. Na época, o java script rodava apenas em navegadores e não havia sistema especifico para rodar JS.

-``Modules``:
Surgiu em 2015. Foi uma solução para rodar nativamente nos navegadores e Node.js.
t

### 2. Qual a diferença entre os dois?
- ``CommonJS´´:
	-Feito para rodar em servidor Node.js de forma síncrono. Exemplo: Quando há o código ``require ()``, a execução do código para e fica esperando o arquivo carregar para só depois continuar.

-``Modules``:
	-Baixa vários arquivos ao mesmo tempo sem travar a aplicação. Ele foi feito dessa maneira para rodar em navegadores e não parar tudo para executar

