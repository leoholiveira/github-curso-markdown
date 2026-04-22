# Desafio de Git - Minha Jornada de Aprendizado

## Sobre este material

Neste arquivo, eu reuni os principais pontos que aprendi no curso de Git.  
A ideia e organizar de forma clara os conceitos, comandos e boas praticas que eu posso aplicar no dia a dia, tanto em projetos pessoais quanto em equipes.

---

## Quem sou eu neste desafio

Durante este desafio, eu assumi o papel de desenvolvedor(a) que:

- esta aprendendo versionamento de codigo de forma estruturada;
- quer sair do uso basico do Git para um fluxo mais profissional;
- precisa documentar o aprendizado em Markdown com exemplos reais.

Meu objetivo foi transformar conteudo teorico em um guia pratico de consulta rapida.

---

## O que eu aprendi no curso

### 1) Fundamentos de versionamento

Eu entendi que o Git nao e apenas "salvar codigo", mas sim:

- manter historico confiavel;
- trabalhar com seguranca em diferentes versoes;
- colaborar com outras pessoas sem sobrescrever trabalho;
- rastrear mudancas com clareza.

### 2) Diferenca entre Git e GitHub

| Ferramenta | O que e | Para que uso |
|---|---|---|
| Git | Sistema de controle de versao distribuido | Versionar codigo localmente e gerenciar historico |
| GitHub | Plataforma de hospedagem de repositorios Git | Compartilhar projetos, revisar codigo e colaborar |

### 3) Estados principais de um arquivo no Git

| Estado | Significado |
|---|---|
| Untracked | Arquivo novo, ainda nao monitorado |
| Modified | Arquivo alterado, mas nao preparado para commit |
| Staged | Arquivo preparado para ser commitado |
| Committed | Alteracao registrada no historico |

---

## Fluxo que eu passei a usar

Este e o fluxo que eu considero mais seguro e organizado:

1. Crio ou atualizo uma branch de trabalho.
2. Faco pequenas alteracoes com objetivo claro.
3. Verifico o estado com `git status`.
4. Adiciono somente o que faz sentido com `git add`.
5. Crio commit com mensagem clara e objetiva.
6. Envio para remoto com `git push`.
7. Abro Pull Request para revisao.

---

## Comandos essenciais que eu mais uso

| Comando | Quando eu uso | Exemplo |
|---|---|---|
| `git init` | Iniciar repositrio local | `git init` |
| `git clone` | Baixar projeto remoto | `git clone https://github.com/user/repo.git` |
| `git status` | Verificar situacao dos arquivos | `git status` |
| `git add` | Preparar alteracoes para commit | `git add .` |
| `git commit -m` | Registrar mudancas | `git commit -m "feat: add login screen"` |
| `git log` | Consultar historico de commits | `git log --oneline` |
| `git branch` | Listar/criar branches | `git branch feature/auth` |
| `git checkout` | Trocar de branch | `git checkout main` |
| `git switch` | Alternativa moderna ao checkout | `git switch -c feature/profile` |
| `git pull` | Trazer atualizacoes do remoto | `git pull origin main` |
| `git push` | Enviar commits para remoto | `git push origin feature/profile` |
| `git diff` | Ver diferencas entre versoes | `git diff` |

> Observacao: eu tento usar commits pequenos e frequentes, pois isso facilita revisao e rollback.

---

## Tipos de commit que eu adotei

Para padronizar mensagens, eu passei a usar um estilo semelhante ao Conventional Commits:

| Tipo | Uso |
|---|---|
| `feat` | Nova funcionalidade |
| `fix` | Correcao de bug |
| `docs` | Alteracoes em documentacao |
| `refactor` | Refatoracao sem mudar comportamento |
| `test` | Criacao/ajuste de testes |
| `chore` | Tarefas de manutencao |

Exemplos:

- `feat: add API integration for students list`
- `fix: handle empty response in alunos controller`
- `docs: update onboarding steps in README`

---

## Estrategia de branches que eu pratico

### Branches principais

- `main`: versao estavel;
- `develop` (quando aplicavel): integracao continua;
- `feature/*`: novas funcionalidades;
- `hotfix/*`: correcoes urgentes em producao.

### Exemplo de fluxo real

```bash
git switch main
git pull origin main
git switch -c feature/cadastro-alunos
# ... desenvolvimento ...
git add .
git commit -m "feat: add create student form"
git push -u origin feature/cadastro-alunos
```

---

## Boas praticas que eu quero manter

- sempre sincronizar com a branch principal antes de iniciar tarefa;
- evitar commits gigantes;
- escrever mensagens de commit explicando o "por que";
- revisar `git diff` antes de commitar;
- nao versionar segredos (`.env`, chaves, tokens);
- usar Pull Request com descricao e checklist.

---

## Erros comuns que eu aprendi a evitar

| Erro | Impacto | Como evitar |
|---|---|---|
| Commitar tudo com `git add .` sem revisar | Pode enviar arquivo indevido | Rodar `git status` e `git diff` antes |
| Trabalhar direto na `main` | Risco alto de quebrar versao estavel | Sempre criar branch de feature |
| Mensagens de commit vagas | Historico confuso | Padronizar com `feat/fix/docs/...` |
| Ignorar conflitos de merge | Introduz bugs silenciosos | Resolver com calma e testar apos merge |

---

## Minha conclusao

Depois deste curso, eu passei a enxergar Git como ferramenta de comunicacao tecnica, nao apenas de armazenamento de codigo.  
Cada commit conta uma parte da historia do projeto, e manter essa historia clara ajuda muito no trabalho em equipe.

Meu proximo passo e evoluir em:

- rebase interativo com seguranca;
- estrategias de release;
- automacao de validacoes no pipeline CI/CD.

---

## Referencias que usei para estudar

- [Documentacao oficial do Git](https://git-scm.com/doc)
- [Pro Git Book](https://git-scm.com/book/pt-br/v2)
- [Documentacao do GitHub](https://docs.github.com/pt)

