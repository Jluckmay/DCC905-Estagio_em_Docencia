# DCC905 — Estágio em Docência

Repositório de apoio às disciplinas **Estágio em Docência I e II** do Programa de Pós-Graduação em Ciência da Computação (PPGCC/DCC/UFMG). Reúne as diretrizes oficiais e **templates LaTeX anonimizados** para a **Proposta de Trabalho** e para o **Relatório Final**, com instruções de preenchimento.

## Estrutura do repositório

```
.
├── 20190802 Disciplina Estagio em Docencia Diretrizes Gerais v2019_2.pdf   # Diretrizes oficiais
├── Template Proposta Estagio/      # Template da Proposta de Trabalho
│   ├── main.tex
│   └── README.md
├── Template Relatorio Final/       # Template do Relatório Final
│   ├── main.tex
│   ├── bibliografia.bib
│   ├── imgs/default/               # Logos institucionais (UFMG e DCC)
│   └── README.md
└── README.md                       # Este arquivo
```

## Conteúdo

| Item | Descrição |
|---|---|
| **Diretrizes (PDF)** | Normas gerais do Estágio em Docência: objetivos, condução, proposta, relatório final, critérios de avaliação (proposta: 50 pts; relatório: 50 pts). |
| **Template Proposta Estagio** | Estrutura exigida: 1. Identificação; 2. Sobre a Disciplina (condução, ementa/programa, bibliografia, avaliação); 3. Atividades; 4. Cronograma. |
| **Template Relatorio Final** | Estrutura exigida: 1. Disciplina/turma apoiada; 2. Atividades conduzidas; 3. Resultados obtidos; 4. Autoavaliação; 5. Sugestões para futuras ofertas. |

Os templates **não contêm dados pessoais**: nomes, matrículas, e-mails, disciplina e resultados foram substituídos por campos entre colchetes `[ ... ]`.

## Como usar os templates

1. Copie a pasta do template desejado para o seu projeto.
2. No início do `main.tex`, preencha os comandos `\newcommand` (bloco de dados da capa/gerais). Eles são reutilizados em todo o documento.
3. Siga as caixas azuis **INSTRUÇÃO** de cada seção e substitua os textos `[ ... ]` pelo seu conteúdo.
4. Ao finalizar, troque `\mostrarinstrucoestrue` por `\mostrarinstrucoesfalse` para ocultar todas as caixas de instrução.
5. Compile o PDF (ver abaixo) e envie pelo Moodle.

### Compilação

Requer TeX Live ou MiKTeX com os pacotes `babel`, `tcolorbox`, `longtable`, `enumitem`, `hyperref` (e `tikz`/`titling`, conforme o template).

```bash
# Proposta de Trabalho
cd "Template Proposta Estagio"
pdflatex main.tex && pdflatex main.tex

# Relatório Final
cd "Template Relatorio Final"
pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex
```

## Fluxo recomendado do estágio

1. **Proposta de Trabalho:** acertar previamente com o professor responsável, enviar o PDF pelo Moodle (`NomeCompletoDoAluno.pdf`) e avisar o coordenador da disciplina por e-mail, com o professor em cópia.
2. **Execução:** cumprir as atividades e o cronograma propostos ao longo do semestre.
3. **Relatório Final:** entregar pelo Moodle ao final do semestre; é avaliado pelo professor responsável (cumprimento dos objetivos, qualidade do apoio, disponibilidade e assiduidade, motivação e desenvoltura).

## Boas práticas

- Use **dados agregados** no relatório (médias, taxas de entrega); nunca cite nomes ou matrículas de alunos (LGPD).
- Mantenha o relatório coerente com a proposta aprovada, justificando eventuais desvios.
- Não versione arquivos temporários de compilação (`.aux`, `.log`, `.out`, `.toc`, `.bbl`, `.blg`).

## Contribuindo

Melhorias aos templates são bem-vindas via *pull request*: faça um fork, crie uma branch, adicione suas alterações e abra o PR descrevendo a mudança. Commits preferencialmente no formato *Conventional Commits* (`docs: ...`, `fix: ...`).

## Referências

- Colegiado do PPGCC/UFMG. *Diretrizes para as Atividades de Estágio em Docência*, 2019.
