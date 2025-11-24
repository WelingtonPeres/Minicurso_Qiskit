
Olá! Seja bem-vindo(a) ao nosso minicurso de Introdução ao Qiskit. 🚀

# Verificação das Ferramentas

Antes de começarmos a programar, vamos fazer uma verificação rápida para garantir que tudo está funcionando como esperado e para que você se familiarize com a ferramenta que usaremos: **VS Code com Jupyter Notebooks**.

> **Está configurando o ambiente em casa?** <details>
>   <summary>Clique aqui para abrir o guia de instalação completo.</summary>
>
>   > Se você não tem Python, VS Code e as extensões necessárias instaladas, por favor, siga nosso guia detalhado antes de continuar.
>
>   ➡️ **[[Guia de Instalação das Ferramentas]]**
>
>   Após concluir a instalação, retorne a este arquivo para fazer a verificação final. </details>

---
### Passo 1: Abrir o Visual Studio Code (VS Code)

Primeiro, localize e abra o Visual Studio Code em seu computador.

*   Procure por **"Visual Studio Code"** no menu de aplicativos ou na área de trabalho e clique para iniciar.

### Passo 2: Criar e Abrir a Pasta do Projeto

Manter nossos arquivos organizados é uma ótima prática.

1.  Crie uma nova pasta em um local de fácil acesso (por exemplo, na Área de Trabalho ou em Documentos) e nomeie-a como `Minicurso_Qiskit`.
2.  Dentro do VS Code, vá ao menu superior e clique em `File > Open Folder...`.
3.  Selecione a pasta `Minicurso_Qiskit` que você acabou de criar.

### Passo 3: Criar seu Primeiro Jupyter Notebook

Agora, vamos criar o tipo de arquivo onde escreveremos todo o nosso código quântico.

1.  Com a pasta aberta no VS Code, pressione o atalho `Ctrl+Shift+P` para abrir a **Paleta de Comandos**.
2.  Na barra de busca que aparecer no topo, comece a digitar `Jupyter: Create New Jupyter Notebook` e pressione `Enter` quando a opção aparecer.
3.  Um novo arquivo chamado `Untitled-1.ipynb` será aberto no editor.

### Passo 4: Executar o Código de Verificação

Este é o teste final para confirmar que tudo está funcionando perfeitamente.

1.  Você verá uma caixa de texto chamada "célula". Clique dentro dela e digite o seguinte código Python:

```python
print("Ambiente configurado!")
```

2.  Para executar o código, você pode:
    *   Clicar no ícone de "Play" (▶️) à esquerda da célula.
    *   Ou, com o cursor na célula, usar o atalho de teclado `Shift + Enter`.

####  O Ponto Crítico: Selecionando o Kernel (*se necessário*)

Na primeira vez que você executar o código, o VS Code pode pedir para você **"Select Kernel"** (Selecionar o Kernel). O Kernel é simplesmente o "motor" Python que executa seu código.

*   Se uma lista de opções aparecer, selecione a versão do Python instalada para o curso. Geralmente, o nome será algo como **`Python 3.x.x`** ou similar.
---

# Criando um Ambiente Virtual

Com nosso ambiente base verificado, vamos dar um passo importante que é considerado uma **boa prática** no desenvolvimento com Python: criar um ambiente virtual.

### Criando e Ativando o Ambiente (Método Padrão do Python)

Vamos usar o módulo `venv`, que já vem instalado com o Python.

#### Passo 1: Abrir o Terminal no VS Code

Dentro do VS Code, com a sua pasta `Minicurso_Qiskit` aberta, abra o terminal integrado:
*   Vá ao menu superior: `Terminal > New Terminal`.
*   Ou use o atalho: `Ctrl + '` (a tecla de acento grave/crase).

#### Passo 2: Criar o Ambiente Virtual

No terminal que você acabou de abrir, digite o seguinte comando e pressione `Enter`:

```bash
python -m venv venv
```

#### Passo 3: Ativar o Ambiente

Agora que o ambiente existe, precisamos "entrar" nele. O comando de ativação muda dependendo do seu sistema operacional.

*   **💻 No Windows (usando PowerShell ou CMD):**
```bash
.\venv\Scripts\activate
```


*   **🍎 No macOS ou 🐧 Linux:**
```bash
source venv/bin/activate    
```

**Sinal de Sucesso:** Você verá o nome do ambiente, `(venv)`, aparecer no início da linha do seu terminal. Isso confirma que seu terminal agora está **dentro** da mochila do projeto!

---

> **Você instalou o Python via Anaconda?**
> <details>
>   <summary>Clique aqui para ver as instruções específicas para Conda.</summary>
>
>   O Anaconda usa seu próprio sistema de gerenciamento de ambientes. Os comandos são diferentes, mas o conceito é o mesmo.
>
>   1.  **Criar o ambiente (no terminal):**
>       ```bash
>       conda create --name qiskit-env python=3.10 -y
>       ```
>       *Isso cria um ambiente gerenciado centralmente pelo Conda, não uma pasta local.*
>
>   2.  **Ativar o ambiente (no terminal):**
>       ```bash
>       conda activate qiskit-env
>       ```
>       *O sinal de sucesso será `(qiskit-env)` no início da linha do terminal.*
> </details>

---

#### Passo 4: Conectar o Jupyter no VS Code ao Novo Ambiente

O seu terminal sabe sobre o ambiente, mas o seu arquivo Jupyter Notebook (`.ipynb`) também precisa saber qual "motor" Python usar.

1.  Abra ou crie um arquivo `.ipynb` no VS Code (como fizemos no passo de verificação).
2.  No canto superior direito da tela, clique onde aparece a versão do Python ou "Select Kernel".
3.  Uma lista de interpretadores Python disponíveis aparecerá no topo. **Selecione o ambiente que você acabou de criar**.
    *   Para `venv`, a opção deve ter um ícone de pasta e o caminho deve incluir a pasta `venv` (ex: `Python 3.10.x ('venv': venv)`).
    *   Para `conda`, a opção deve incluir o nome `qiskit-env` (ex: `Python 3.10.x ('qiskit-env': conda)`).
4.  Pronto! Agora, qualquer código que você executar nesse notebook usará o Python e as bibliotecas de dentro do seu ambiente virtual.

---
# Instalar o Qiskit

No terminal integrado do VS Code (onde seu ambiente virtual está ativo), copie e cole o seguinte comando. Ele instalará todos os componentes do Qiskit que precisaremos para o minicurso.

```bash
pip install qiskit
pip install qiskit[visualization]
pip install qiskit-aer
pip install qiskit_ibm_runtime
```

A melhor maneira de confirmar que tudo foi instalado corretamente é pedir ao Qiskit para nos dizer sua própria versão, diretamente de dentro de um Jupyter Notebook.

1.  Abra ou volte para o seu arquivo `.ipynb` no VS Code.
2.  **Importante:** Verifique se o Kernel selecionado no canto superior direito é o seu ambiente virtual (`venv` ou `qiskit-env`).
3.  Crie uma nova célula de código e digite o seguinte:

```python
import qiskit

print("Versão do Qiskit instalada:")
print(qiskit.__version__)
```
