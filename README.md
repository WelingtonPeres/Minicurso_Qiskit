
Olá! Seja bem-vindo(a) ao nosso minicurso de Introdução ao Qiskit. 🚀

[Banner]([../docs_minicurso/Banner.png.png](https://github.com/WelingtonPeres/Minicurso_Qiskit/blob/f26bdb409187f4c9a11bc1f4e980f6126b4e4190/docs_minicurso/Banner.png))
# Verificação das Ferramentas

Antes de começarmos a programar, vamos fazer uma verificação rápida para garantir que tudo está funcionando como esperado e para que você se familiarize com a ferramenta que usaremos: **VS Code com Jupyter Notebooks**.

<div align="center">
  <img src="./VScodeJupyter.jpg" width="400px" />
</div>


> **Está configurando o ambiente em casa?** <details>
>   <summary>Clique aqui para abrir o guia de instalação completo.</summary>
>
>   > Se você não tem Python, VS Code e as extensões necessárias instaladas, por favor, siga nosso guia detalhado antes de continuar.
>
>    **[[Guia de Instalação das Ferramentas]]**
>
>   Após concluir a instalação, retorne a este arquivo para fazer a verificação final. </details>

---
### Passo 1: Abrir o Visual Studio Code (VS Code)

Primeiro, localize e abra o Visual Studio Code em seu computador.

*   Procure por **"Visual Studio Code"** no menu de aplicativos ou na área de trabalho e clique para iniciar.
---
### Passo 2: Criar e Abrir a Pasta do Projeto

Manter nossos arquivos organizados é uma ótima prática.

1.  Crie uma nova pasta em um local de fácil acesso (por exemplo, na Área de Trabalho ou em Documentos) e nomeie-a como `Minicurso_Qiskit`.
2.  Dentro do VS Code, vá ao menu superior e clique em `File > Open Folder...`.
3.  Selecione a pasta `Minicurso_Qiskit` que você acabou de criar.
---
### Passo 3: Criar seu Primeiro Jupyter Notebook

Agora, vamos criar o tipo de arquivo onde escreveremos todo o nosso código quântico.

1.  Com a pasta aberta no VS Code, pressione o atalho `Ctrl+Shift+P` para abrir a **Paleta de Comandos**.
2.  Na barra de busca que aparecer no topo, comece a digitar `Jupyter: Create New Jupyter Notebook` e pressione `Enter` quando a opção aparecer.
3.  Um novo arquivo chamado `Untitled-1.ipynb` será aberto no editor.

---
### Passo 4: Executar o Código de Verificação

Este é o teste final para confirmar que tudo está funcionando perfeitamente.

1.  Você verá uma caixa de texto chamada "célula". Clique dentro dela e digite o seguinte código Python:

```python
print("Ambiente configurado!")
```

2.  Para executar o código, você pode:
    *   Clicar no ícone de "Play" à esquerda da célula.
    *   Ou, com o cursor na célula, usar o atalho de teclado `Shift + Enter`.

####  O Ponto Crítico: Selecionando o Kernel (*se necessário*)

Na primeira vez que você executar o código, o VS Code pode pedir para você **"Select Kernel"** (Selecionar o Kernel). O Kernel é simplesmente o "motor" Python que executa seu código.

*   Se uma lista de opções aparecer, selecione a versão do Python instalada para o curso. Geralmente, o nome será algo como **`Python 3.x.x`** ou similar.

---
# Instalar o Qiskit

No terminal integrado do VS Code, copie e cole o seguinte comando. Ele instalará todos os componentes do Qiskit que precisaremos para o minicurso.

```bash
pip install qiskit
pip install qiskit[visualization]
pip install qiskit_aer
pip install qiskit_ibm_runtime
```

A melhor maneira de confirmar que tudo foi instalado corretamente é pedir ao Qiskit para nos dizer sua própria versão, diretamente de dentro de um Jupyter Notebook.

1.  Abra ou volte para o seu arquivo `.ipynb` no VS Code.
2.  **Importante:** Verifique se o Kernel selecionado no canto superior direito é o seu python
3.  Crie uma nova célula de código e digite o seguinte:

```python
import qiskit

print("Versão do Qiskit instalada:")
print(qiskit.__version__)
```
