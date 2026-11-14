# bun-monorepo-template — checklist da primeira release para usuários externos

Use uma cópia deste checklist para o candidato que será distribuído. Registre versão, commit, canal, plataformas, responsável e data da decisão. Uma caixa marcada precisa apontar para um teste, relatório, captura ou decisão. Para um item inaplicável, registre o motivo.

**Referências do repositório** — [README.md](../../README.md) · [package.json](../../package.json)

## Escopo e aceite do produto

- [ ] Definir público, fluxo principal, funcionalidades incluídas, limites conhecidos e plataformas suportadas. Registrar o que impede o lançamento e quem decide.
- [ ] Inicializar os serviços anunciados num clone novo, verificar saúde e comunicação a partir de um workspace Bun.
- [ ] Reiniciar os contêineres, verificar persistência e documentar quais comandos removem volumes e como trocar credenciais iniciais.
- [ ] Executar esses cenários no candidato final com dados fictícios e guardar resultados esperados, observados e versão testada.

## Distribuição do starter ou coleção

- [ ] Enumerar variantes e versões suportadas e fixar uma tag de origem. Verificar instruções, pré-requisitos, termos de reuso e licenças dos recursos incluídos.
- [ ] Gerar uma cópia com nome novo em ambiente vazio. Substituir identificadores de exemplo e executar build e testes seguindo apenas o guia entregue.
- [ ] Conferir que arquivos gerados, dados locais, credenciais e configurações pessoais ficaram fora do pacote. Documentar atualização e diferenças entre variantes.

## Qualidade e recuperação

- [ ] Reproduzir o build em ambiente limpo a partir do commit escolhido, com dependências e ferramentas identificadas. Executar os testes e verificações estáticas do projeto e guardar os resultados.
- [ ] Cobrir primeiro uso, fluxo principal, cancelamento, entrada inválida e falha de dependência. Conferir mensagens de erro e retomar sem perder trabalho.
- [ ] Medir inicialização e o fluxo mais custoso com uma carga representativa. Registrar dispositivo, volume, limite aceitável e resultado.
- [ ] Verificar acessibilidade da interface entregue, incluindo teclado, foco, rótulos, contraste ou mensagens legíveis no terminal. Revisar idiomas, unidades e formatos anunciados.
- [ ] Quando houver dados persistidos, testar migração em cópia, backup, restauração e contagem ou comparação dos registros recuperados. Incluir dados de betas anteriores se houver.

## Segurança, privacidade e direitos

- [ ] Inventariar dados coletados, locais de armazenamento, transferências, retenção e exclusão. Conferir que política de privacidade e telas descrevem o comportamento efetivo.
- [ ] Revisar permissões, autenticação e limites entre usuários ou processos. Testar acesso negado e revogação com contas ou perfis de teste.
- [ ] Inspecionar pacote, exemplos, logs e histórico que será disponibilizado em busca de credenciais, dados pessoais e material interno. Resolver exposições e revisar dependências com alertas relevantes.
- [ ] Confirmar direito de distribuir código, dados, ícones, fontes, marcas e conteúdo de terceiros. Incluir licença ou termos, atribuições e um contato para questões de segurança.

## Entrega e operação

- [ ] Definir gratuito, pago ou uso restrito e comunicar os limites. Se houver cobrança, testar compra, falha, restauração, cancelamento ou reembolso e conciliação no canal escolhido.
- [ ] Preparar página ou ficha de distribuição, instruções de instalação e remoção, notas da versão, requisitos e contato de suporte. Conferir os links como usuário externo.
- [ ] Vincular tag ou identificador imutável ao artefato ou deploy. Registrar hash ou ID do build e testar o acesso com a mesma permissão de um usuário externo.
- [ ] Definir como detectar falhas respeitando a privacidade. Ensaiar diagnóstico com dados fictícios, triagem de um relato e contato com o responsável.
- [ ] Ensaiar retirada do pacote, reversão do deploy ou entrega de versão corretiva. Verificar compatibilidade de dados e registrar como avisar os usuários.
- [ ] Pedir a uma pessoa fora do desenvolvimento que siga as instruções e conclua o fluxo principal. Registrar problemas, corrigir os bloqueadores e repetir o teste afetado.

## Decisão de publicação

| Candidato e canal | Responsável e data | Evidências | Pendências aceitas, responsável e prazo | Decisão |
|---|---|---|---|---|
| A preencher | A preencher | Links do build e dos testes | A preencher | Pendente |

Autorizar quando os cenários essenciais passarem no artefato entregue e as pendências restantes tiverem decisão registrada. Depois da publicação, conferir acesso pelo canal final, executar o fluxo principal e registrar a primeira rodada de suporte.
