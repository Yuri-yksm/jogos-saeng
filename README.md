# Jogos internos SAENG · AAIFEC Biônicos

Site com chaves, tabelas e resultados dos jogos internos.

- `index.html`: o site.
- `dados.json`: inscritos e placares. É o único arquivo que muda durante os jogos, e quem muda é o próprio site quando o organizador clica em **Salvar e publicar**.

## Como funciona o acesso

- **Alunos** abrem o link e só leem. A página busca placares novos sozinha a cada minuto.
- **Organizador** entra em **Área do organizador** (rodapé do site) com uma chave de acesso do GitHub. Sem essa chave, ninguém consegue alterar nada.

## Publicar no GitHub Pages

1. Crie um repositório **público** chamado `jogos-saeng` (pode ser outro nome).
2. Clique em **Add file → Upload files**, envie `index.html`, `dados.json` e este `README.md`, e depois clique em **Commit changes**.
3. Vá em **Settings → Pages**. Em *Build and deployment*, escolha **Deploy from a branch**, depois a branch **main** e a pasta **/ (root)**, e clique em **Save**.
4. Em 1 ou 2 minutos o site fica no ar em `https://SEU-USUARIO.github.io/jogos-saeng/`.

## Criar a chave do organizador

1. No GitHub, clique na sua foto e vá em **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Preencha:
   - **Expiration:** uma data logo depois dos jogos.
   - **Repository access:** *Only select repositories*, e escolha `jogos-saeng`.
   - **Permissions → Repository permissions → Contents:** *Read and write*.
3. Clique em **Generate token** e copie a chave (começa com `github_pat_`).
4. No site, clique em **Área do organizador** no rodapé, cole a chave e clique em **Entrar**.

A chave fica guardada só naquele navegador. Em computador emprestado, clique em **Esquecer minha chave neste navegador** ao terminar. Nunca coloque a chave dentro de arquivos do repositório.

## Durante os jogos

1. Entre no **Modo organizador** e lance os placares.
2. Clique em **Salvar e publicar**. Em cerca de 1 minuto todo mundo vê.
3. As súmulas e as folhinhas de campeão em PDF aparecem só no modo organizador.

## Domínio próprio

Se usar um domínio que não seja `github.io`, abra `index.html` e preencha `owner` (seu usuário) e `repo` (nome do repositório) na linha `const CONFIG = ...`.
