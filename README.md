# Projemetria — Versão 7 | Entregas conectadas às atividades

Protótipo navegável em um único arquivo HTML. Abra `index.html` no navegador.

## O que mudou

- **Meu negócio** reúne Canvas, entregas do MVP, Kanban de atividades e visão financeira em uma mesma página. Não há mais "Atividades do negócio" no menu lateral.
- **Entrega antes da atividade**: só é possível criar uma nova atividade depois de cadastrar uma entrega do MVP no nível correspondente (negócio, projeto ou iniciativa).
- **Vínculo obrigatório**: na criação ou edição da atividade, o usuário escolhe a entrega do mesmo negócio/projeto/iniciativa.
- **Progresso automático**: cada entrega apresenta a proporção de atividades concluídas (concluídas / total de atividades vinculadas). Uma entrega sem atividades fica em 0%. O progresso geral das entregas é a média simples desses percentuais.
- **Status dinâmicos**: alterar uma atividade para “A fazer”, “Em andamento” ou “Concluída” atualiza imediatamente o progresso da entrega.
- **Canvas e MVP por nível**: cada negócio, projeto ou iniciativa possui suas próprias entregas e atividades; dados não se misturam.
- **Dashboard**: gráfico fixo de progresso das entregas, disponível na visão geral e nos dashboards de projetos/iniciativas.
- **Edição/exclusão**: entregas podem ser renomeadas e atividades podem ser editadas, reatribuídas ou excluídas. Para não criar registros órfãos, uma entrega vinculada a atividades não pode ser excluída até que elas sejam reatribuídas ou excluídas.
- **Interface**: mantém verde-lima/grafite, modos claro/escuro, áreas, pessoas, financeiro, editais e anexos da versão anterior.

## Como testar

1. Cadastre um negócio.
2. Abra **Meu negócio** e crie uma entrega em **1 · Entregas do MVP**.
3. Em **2 · Atividades do negócio**, adicione atividades e selecione a entrega correspondente.
4. Marque uma atividade como **Concluída** e observe a barra de progresso da entrega.
5. Crie um projeto/iniciativa e repita o fluxo na aba **Atividades**.
6. Consulte o **Dashboard** para acompanhar o progresso consolidado das entregas.

## Limitações

Protótipo front-end, sem servidor ou autenticação. Os dados são armazenados localmente no navegador, sem sincronização. Não utilize dados confidenciais. Arquivos de fomento podem depender do suporte do navegador a IndexedDB.

## Tecnologias

HTML5, CSS, Tailwind CSS (CDN) e JavaScript. A interface usa fontes externas; para visual completo é necessária conexão à internet.
