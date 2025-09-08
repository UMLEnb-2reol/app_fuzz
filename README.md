# Repositório das aulas

---


O código usado está num repositório público da trilha.


# Slides das aulas

O material apresentado está publicado na plataforma do curso.


# Primeiro teste, passo a passo

```sh
npm init -y
npm install -D typescript tsup tsx
echo "node_modules" > .gitignore
npx tsc --init
```

Isso gera o arquivo de configuração do compilador. Existe um repositório público com as opções que devem ser usadas nesse arquivo.

A orientação seguinte foi declarar o campo de tipo como módulo no manifesto do projeto.

Como penúltimo passo, criar o arquivo de entrada com uma única linha imprimindo uma saudação no terminal.

Como último passo, declarar o script de desenvolvimento que inicializa a aplicação:

![script start:dev](images/script-de-desenvolvimento.png)


# Executando em modo de depuração pelo manifesto (no editor)

![debugging an application through package.json](images/depuracao-pelo-manifesto.png)


# Terminal de depuração JavaScript do editor

É uma janela dentro do próprio editor:

![javascript debug terminal](images/terminal-de-depuracao.png)


# Problema de espaço de trabalho não confiável no Windows

Tive esse problema no Windows e o assistente que uso devolveu uma resposta em português, que reproduzo em resumo:

Ele explicou que o editor tem um modo de segurança em que o espaço de trabalho começa como não confiável, e que nesse modo algumas funções, entre elas a depuração, ficam bloqueadas. Para liberar, listou quatro caminhos: aceitar o aviso na faixa que aparece no topo da janela; usar a paleta de comandos e procurar o comando de confiança do espaço de trabalho; entrar nas configurações, localizar a seção de segurança do espaço de trabalho e habilitar a opção; ou ainda criar o arquivo de preferências da pasta de configuração na raiz do projeto com a chave de confiança ligada. Ao final sugeriu reiniciar o editor, conferir que o aviso sumiu e tentar depurar novamente, e lembrou de olhar extensões e políticas de segurança da empresa caso persistisse.

Essas dicas não funcionaram comigo; acredito que por causa das políticas de rede da empresa. Vou tentar em casa depois.


# Barra lateral de depuração

![left debugging bar](images/barra-de-depuracao.png)


# Vendo valores de variáveis

![seeing variables values](images/vendo-valores.png)

Comentário: com um ponto de parada definido, dá para ver o valor da variável até aquele ponto.


# Bloco global

![global block](images/bloco-global.png)


# Bloco de vigilância

Existe um painel para acompanhar o valor de uma variável.

![watch block](images/painel-de-vigilancia.png)

Como a imagem mostra, dá para acompanhar tanto funções quanto variáveis.

Outro detalhe: nesse painel há um botão de adicionar, à direita, para incluir novos itens na vigilância.


# Pilha de chamadas

![call stack](images/pilha-de-chamadas.png)

Nesse painel aparece a ordem das funções chamadas durante a execução.


# Scripts carregados

![loaded scripts](images/scripts-carregados.png)


# Pontos de parada

![breakpoints](images/pontos-de-parada.png)

Os números circulados em vermelho indicam a linha do ponto de parada em cada arquivo.


# Controle de fluxo

![flow control](images/controle-de-fluxo.png)

No canto superior esquerdo da imagem ficam os controles que permitem avançar, pausar e seguir durante a depuração.


# Configuração de depuração

![debug configuration](images/configuracao-de-depuracao.png)

Na imagem acima a orientação foi clicar no link (é um link, não um botão) que cria o arquivo de configuração de execução.

Depois, escolher a opção de ambiente de execução.

![basic launch json file](images/arquivo-de-execucao-basico.png)

Como se vê, o editor cria um arquivo básico de configuração de execução.

A sugestão seguinte foi limpar todo o conteúdo da lista de configurações e depois usar o botão de adicionar configuração, mostrado na imagem a seguir:

![add configurations button](images/botao-adicionar-configuracao.png)

E então escolher a opção de anexar a um processo.

Comentário: esse arquivo controla o comportamento do editor ao depurar uma aplicação.


# Rodando em modo de depuração ao anexar a processo

![running in attach to process](images/anexando-a-processo.png)

Na imagem a sugestão foi escolher a execução do script de desenvolvimento. Não sei se faz muito sentido, porque configuramos a opção de anexar por identificador de processo; preciso estudar melhor esse modo de depuração depois.