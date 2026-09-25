# Ambiente de Desenvolvimento

Este guia explica como preparar o ambiente e como cada integrante trabalha na sua branch. Há duas opções: **rodar localmente** (JupyterLab + GitHub Desktop) ou **usar o Google Colab**. As duas funcionam juntas: cada integrante pode escolher a sua.

## Estrutura do projeto

| Caminho | Conteúdo |
|---|---|
| `trabalho.ipynb` | Notebook de entrega, já dividido por etapa e responsável |
| `dados/` | Arquivo CSV utilizado |
| `requirements.txt` | Bibliotecas necessárias (NumPy, Pandas, Matplotlib, JupyterLab) |
| `Documentos/Tarefas.md` | Divisão de tarefas e cronograma |
| `Documentos/Ambiente.md` | Este guia |

## Regras gerais (valem para as duas opções)

1. Cada integrante trabalha **somente na sua branch** (`rafael` ou `luan`), criada a partir da `master`. Nunca commite direto na `master`.
2. Edite **somente as células da sua parte** no notebook. O responsável de cada célula está indicado no título dela.
3. **Não salve as saídas das células** no repositório. Elas geram conflitos no merge.
4. Quando terminar uma parte, abra um **Pull Request** da sua branch para a `master` e peça para o outro revisar.
5. Depois de cada merge na `master`, **atualize a sua branch** antes de continuar trabalhando.

## Por onde começar (ordem sugerida)

A ordem sugerida, com caixas para marcar o que já foi feito, está no documento [Ambiente (Google Docs)](https://docs.google.com/document/d/1luwelG_18si0I3a87AAJE6uz6xtEtsyk9ENAU7kr8S4/edit?tab=t.0).

---

## Opção 1: Ambiente local (JupyterLab + GitHub Desktop)

O Git é usado pelo **GitHub Desktop**, um programa com botões que evita digitar comandos. É o caminho recomendado para quem está começando.

### Etapa 1: Instalar os programas (só na primeira vez)

1. **Python 3**: baixe em <https://www.python.org/downloads/>. Na instalação no Windows, marque **Add Python to PATH**.
2. **GitHub Desktop**: baixe em <https://desktop.github.com/> e instale.
3. Abra o GitHub Desktop e entre com a sua conta: *File → Options → Accounts → Sign in*.

### Etapa 2: Clonar o repositório (só na primeira vez)

1. *File → Clone repository*.
2. Na aba **GitHub.com**, escolha `Rafa516/projeto-IPCC-IFSP`.
3. Em **Local path**, escolha a pasta onde o projeto vai ficar.
4. Clique em **Clone**.

### Etapa 3: Criar as branches (só uma vez, feito pelo Rafael)

1. Clique em **Current branch** (barra superior) e selecione a `master`.
2. Clique em **Fetch origin** para garantir que a `master` está atualizada.
3. Clique em **Current branch → New branch**.
4. Digite `rafael`, confirme que está baseada na `master` e clique em **Create branch**.
5. Clique em **Publish branch** para enviar a branch ao GitHub.
6. Volte para a `master` e repita os passos 3 a 5 com o nome `luan`.

### Etapa 4: Entrar na sua branch

1. Clique em **Fetch origin**.
2. Clique em **Current branch** e escolha a sua branch (`rafael` ou `luan`).

> Sempre confira em **Current branch** se você está na **sua** branch antes de começar a trabalhar.

### Etapa 5: Criar o ambiente virtual e instalar as bibliotecas (só na primeira vez)

1. No GitHub Desktop, vá em *Repository → Open in Command Prompt* (ou *Open in Terminal*). Um terminal abre já na pasta do projeto.
2. Rode:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

> No Linux/Mac, troque a segunda linha por `source .venv/bin/activate`.

### Etapa 6: Trabalhar no notebook

1. Abra o terminal pelo GitHub Desktop (*Repository → Open in Command Prompt*).
2. Rode:

```bash
.venv\Scripts\activate
jupyter lab
```

3. O JupyterLab abre no navegador. Abra o `trabalho.ipynb` e edite **apenas as células da sua parte**.

### Etapa 7: Commitar e enviar

1. No JupyterLab, limpe as saídas: *Kernel → Restart Kernel and Clear All Outputs*.
2. Salve o notebook (`Ctrl+S`).
3. No GitHub Desktop, na aba **Changes**, confira os arquivos alterados (deve aparecer o `trabalho.ipynb`).
4. No campo **Summary** (canto inferior esquerdo), escreva o que foi feito. Ex.: `Etapa 2: arrays e slicing com NumPy`.
5. Clique em **Commit to rafael** (ou **luan**). Confira se o botão mostra o nome da **sua** branch.
6. Clique em **Push origin** (barra superior) para enviar ao GitHub.

### Etapa 8: Abrir um Pull Request para a `master`

1. Depois do push, clique em **Create Pull Request** (ou *Branch → Create pull request*).
2. O navegador abre o GitHub. Confira se está **da sua branch para a `master`**.
3. Escreva um título, descreva o que foi feito e clique em **Create pull request**.
4. Avise o outro integrante para revisar.

### Etapa 9: Atualizar a sua branch com a `master` (após cada merge)

1. Com a sua branch selecionada, clique em **Fetch origin**.
2. Vá em *Branch → Update from master*.
3. Clique em **Push origin**.

<details>
<summary>Alternativa: os mesmos passos pelo terminal</summary>

```bash
# Clonar
git clone https://github.com/Rafa516/projeto-IPCC-IFSP.git
cd projeto-IPCC-IFSP

# Criar as branches (só o Rafael, uma vez)
git checkout master
git checkout -b rafael && git push -u origin rafael
git checkout master
git checkout -b luan && git push -u origin luan

# Entrar na sua branch
git fetch
git checkout rafael           # ou: luan

# Commitar e enviar
git add trabalho.ipynb
git commit -m "Descreva o que foi feito"
git push

# Atualizar a sua branch com a master
git checkout master
git pull
git checkout rafael           # ou: luan
git merge master
git push
```

</details>

---

## Opção 2: Google Colab

O Colab já vem com NumPy, Pandas e Matplotlib instalados, então não é preciso instalar nada.

### Etapa 1: Pré-requisitos (só na primeira vez)

1. Ter acesso de **colaborador** no repositório: o dono adiciona em *GitHub → Settings → Collaborators*.
2. As branches `rafael` e `luan` já devem existir no GitHub (etapa 3 do ambiente local).

### Etapa 2: Configurar o Colab para não salvar as saídas (só na primeira vez)

1. Abra o notebook no Colab (etapa 3).
2. Vá em *Editar → Configurações do notebook*.
3. Marque **"Omitir saída das células de código ao salvar este notebook"** e clique em *Salvar*.

### Etapa 3: Abrir o notebook a partir da sua branch

1. Acesse <https://colab.research.google.com>.
2. Vá em *Arquivo → Abrir notebook → aba GitHub*.
3. Autorize o acesso ao GitHub (e marque *Incluir repositórios privados*, se o repositório for privado).
4. Escolha o repositório `Rafa516/projeto-IPCC-IFSP`, a **sua branch** e o arquivo `trabalho.ipynb`.

### Etapa 4: Carregar o arquivo CSV

O Colab não enxerga a pasta `dados/` do repositório. Há duas formas de resolver:

- **Repositório público:** ler o CSV direto do GitHub. A célula de configuração do notebook pode tentar o caminho local e, se não encontrar, usar o link:

  ```python
  import os
  CAMINHO_DADOS = "dados/dados.csv"
  if not os.path.exists(CAMINHO_DADOS):  # rodando no Colab
      CAMINHO_DADOS = "https://raw.githubusercontent.com/Rafa516/projeto-IPCC-IFSP/master/dados/dados.csv"
  ```

- **Repositório privado:** enviar o arquivo manualmente pelo ícone de pasta na barra lateral do Colab, criar a pasta `dados` e colocar o CSV dentro dela. O arquivo é apagado quando a sessão do Colab termina, então é preciso repetir a cada sessão.

### Etapa 5: Trabalhar no notebook

Edite apenas as células da sua parte e rode com *Ambiente de execução → Executar tudo* para conferir.

### Etapa 6: Salvar na sua branch do GitHub

1. Vá em *Arquivo → Salvar uma cópia no GitHub*.
2. Escolha o repositório `Rafa516/projeto-IPCC-IFSP` e a **sua branch** (nunca a `master`).
3. Mantenha o caminho `trabalho.ipynb`.
4. Escreva uma mensagem de commit descrevendo o que foi feito.
5. Desmarque *Incluir um link para o Colab*, para não alterar o notebook.
6. Clique em *OK*. O Colab faz o commit direto na branch.

### Etapa 7: Atualizar a sua branch com a `master` (após cada merge)

No Colab não há `git merge`. Faça pelo site do GitHub:

1. Abra um Pull Request **da `master` para a sua branch** e faça o merge.
2. Depois, **reabra o notebook no Colab a partir do GitHub** (etapa 3).

> **Atenção:** não continue editando em uma aba antiga do Colab depois de um merge. Ao salvar, ela sobrescreve as mudanças mais novas da branch.

---

## Juntando as partes (Pull Request)

### Pelo GitHub Desktop

1. Confira em **Current branch** se você está na sua branch e se não há nada pendente na aba **Changes**.
2. Clique em **Push origin** para garantir que tudo foi enviado.
3. Vá em *Branch → Create pull request*. O navegador abre o GitHub.
4. Confira se está **da sua branch para a `master`** (`base: master ← compare: rafael`, ou `luan`).
5. Escreva um título, descreva o que foi feito e clique em **Create pull request**.
6. O outro integrante abre o Pull Request no GitHub, revisa o código e clica em **Merge pull request → Confirm merge**.
7. Depois do merge, os dois atualizam as suas branches no GitHub Desktop:
   1. Clique em **Fetch origin**.
   2. Vá em *Branch → Update from master*.
   3. Clique em **Push origin**.

### Se aparecer conflito

1. Ao fazer *Branch → Update from master*, o GitHub Desktop avisa quais arquivos estão em conflito.
2. Clique em **Open in Visual Studio Code** (ou no editor instalado) ao lado do `trabalho.ipynb`.
3. Resolvam juntos, mantendo as células de cada responsável.
4. Salve o arquivo, volte ao GitHub Desktop e clique em **Continue merge**.
5. Clique em **Push origin**.

> Quem usa o Colab atualiza a branch pelo site do GitHub (etapa 7 do Colab).
