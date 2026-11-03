# Projemetria — Protótipo V5

**Gestão de ideias, projetos, pessoas, financeiro, dashboard e editais de fomento.**

## Executar

Abra `index.html` no navegador. O front-end é construído com HTML5, Tailwind CSS (CDN), CSS próprio e JavaScript. Não é necessário instalar pacotes. Para disponibilidade estável das fontes e Tailwind é recomendável ter acesso à internet; o layout principal também contém CSS próprio.

Você começa sem dados de demonstração. Crie um **espaço** (pessoal, startup ou empresa), depois adicione projetos. O espaço consolida os projetos sem que seja necessário passar por etapas obrigatórias.

## Navegação

- **Início:** orientações e visão do trabalho.
- **Meu espaço:** Canvas e MVP, finanças e consolidação da iniciativa.
- **Projetos:** visão geral, Canvas e MVP, Kanban de tarefas, financeiro, equipe e arquivos, dashboard e editais.
- **Pessoas:** cadastro único e custos de referência; a alocação define a participação e o custo estimado por projeto.
- **Dashboard:** um conjunto **fixo**, automático e interativo de indicadores, não exige configuração de métricas. Mostra receitas, despesas, resultado registrado, aportes, evolução mensal, distribuição de tarefas, orçamento, estimativa de equipe, fomento e movimentações.
- **Editais e fomento:** acompanha tanto editais gerais da iniciativa quanto os vinculados a projetos.

## Dashboard

Filtros de período (30 dias, 90 dias, 12 meses, tudo), filtro por projeto no dashboard geral, seleção de uma coluna mensal para explorar os lançamentos, exportação CSV, indicadores e visualização atualizados após os cadastros.

- **Resultado registrado** = receitas menos despesas efetivamente registradas.
- **Aportes** são mostrados separadamente, **não são receitas**.
- Custos mensais de pessoal são **estimativas** e não entram automaticamente no resultado realizado.
- O resultado não é lucro contábil, pois não considera automaticamente impostos, apropriação de custos, competências ou outras regras contábeis.
- O filtro de data atua sobre as movimentações; tarefas, orçamentos, alocações e status dos editais refletem o cadastro atual.

## Editais e fomento

Cada edital contém: nome, referência, instituição, modalidade, iniciativa/projeto vinculado, responsável, situação, encerramento das inscrições, data de inscrição, previsão de resultado, valores solicitado e aprovado, endereço oficial, requisitos, regras de uso, contrapartidas, prestação de contas e observações.

Estados disponíveis: Em preparação, Inscrito, Em análise, Aprovado, Não aprovado, Contratado e Encerrado.

Ao abrir um edital, é possível consultar tudo e anexar/baixar **PDFs de até 15 MB** (edital, proposta, comprovante de inscrição etc.). Metadados dos anexos ficam em `localStorage`; arquivos PDF binários ficam em **IndexedDB** no navegador.

**Regra de caixa:** o valor pedido e o aprovado não viram receita nem dinheiro recebido automaticamente. Use **Registrar recebimento** em um edital para lançar um **aporte efetivamente recebido**, vinculado a ele. O valor recebido será calculado com base nesses lançamentos financeiros, sem duplicidade no consolidado.

## Limitações do protótipo

- Sem autenticação, servidor, sincronização entre dispositivos ou autorização de acesso. **Não colocar documentos sigilosos ou dados pessoais sensíveis**.
- Dados e PDFs ficam **somente no navegador e no perfil usado para abrir o protótipo**. A limpeza dos dados do navegador pode apagá-los. Abrir por outro endereço/origem pode dar acesso a outro conjunto de dados.
- É um front-end para validação de produto, não um sistema financeiro ou contábil homologado.
- O controle de recebimentos depende de lançar o aporte no financeiro; não consulta banco nem API de editais.
- Sem integração ou consulta automática a plataformas de fomento. O usuário informa as regras conforme o edital oficial.

## Estrutura

`index.html` — protótipo interativo autocontido com HTML, CSS e JavaScript.

`preview-*.png` — imagens de avaliação visual da interface (podem conter informações fictícias inseridas apenas durante os testes; não são dados pré-carregados no produto).
