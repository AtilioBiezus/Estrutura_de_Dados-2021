<h1 align="center">Pilhas - UNISEP 2021</h1>

<h2>-- Script JS --</h2>

<h3>Temos três funções principais e essenciais para se utilizar dentro de Pilhas:</h3>
<ul> 
    <li>push() - Utilizado para adicionar itens dentro de uma pilha</li>
    <li>pop() -  Utilizado para remover um item por vez da pilha</li>
    <li>clean() - Utilizado para limpar a pilha inteira</li>
</ul>

``` 
    this.push = function(){
        
        const value = document.getElementById("valorAddPilha").value;

        if(!value){
            alert("Informe um valor!");
            return false;
        }

        itensPilha.push(value);
        this.createItemStack(value);
        this.updateDataStack();
        console.table(itensPilha);

        //Limpando o input
        document.getElementById("valorAddPilha").value = "";
        this.updateDataStack();
    };

    this.pop = function(){

        //Remove da tela
        const lastIndex = document.getElementById(itensPilha.length);
        lastIndex.remove();


        //Remove do vetor
        itensPilha.pop();
        this.updateDataStack();
    };

    this.clean = function(){

        document.getElementById("pilha").innerHTML = "";
        itensPilha = [];
        this.updateDataStack();

    };

```

<h2>-- Design --</h2>

<h3>Dentro do styles.css foi feito todo o design da página web desta aplicação</h3>

<ul> 
    <li>Dentro de alguns designs feitos, o dos botões contendo as funções pop(), push() e clean():</li>
</ul>

```
#control-button > button {

    color: white;
    border: none;
    width: 110px;
    height: 35px;
    font-size: 18px;
    box-shadow: 6px 7px 15px -5px rgba(122,109,122,1); /* Faz a sombra nos buttons*/
    border-radius: 5px;
    cursor: pointer;

}
```

<h2>-- Index --</h2>

<h3>Utilizado para fornecer o tamplate para a página toda</h3>

<ul> 
    <li>Dentro deste foi feito a implementação dos botões, contendo as funções pop(), push() e clean():</li>
</ul>

```
    <div id="control-button">

                    <button type="button" class="btnPush"
                        onclick="pilha.push()">
                        Push
                    </button>
                    <button type="button" class="btnPop"
                    onclick="pilha.pop()">
                        Pop
                    </button>  

                    <button type="button" class="btnClear"
                    onclick="pilha.clean()">
                        Clean
                    </button>
                    
    </div>
```