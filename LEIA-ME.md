# Julio Training OS V6.0.0

Atualização preparada em 30/10/2026 a partir do app publicado em https://sebpitstoprog.github.io/julio-training-os./index.html.

## O que mudou

- Agachamento hack substituído por agachamento livre no LOWER B, mantendo 3 séries de 8–12 repetições. O LEGS A continua com agachamento livre, 3 séries de 6–8. Demais séries e faixas da ficha preservadas.
- Sessões vazias bloqueadas; estados de rascunho, parcial e concluído.
- Campos numéricos validados, RIR opcional e identificação do equipamento.
- Movimento explícito para puxada/barra fixa, afundo/passada e abdômen.
- Abdômen por repetições ou segundos; mudanças de movimento/unidade limpam os valores desse exercício mediante confirmação.
- Histórico clicável com filtros; abertura da ficha e dos valores completos da sessão.
- Última sessão comparável no próprio exercício; gráficos e tabelas por exercício.
- Comparação de repetições quando carga e quantidade de séries são iguais; checagem da faixa da ficha.
- Volume-base e volume de extensões separados; rascunhos fora dos totais.
- Pesagens com data própria, gráfico e média das pesagens disponíveis nos sete dias até o último registro.
- Cronômetro fixo, início automático opcional, som e vibração quando permitidos.
- Backups JSON completos, CSV analítico, prévia/validação de importação e cópia de segurança antes de substituir ou limpar.
- Fichas e nomes salvos como fotografia da sessão. IDs permanentes substituem a dependência de posição.
- Migração V4/V5 conserva a origem, o nome do hack e valores antigos. Registros legados ficam fora dos comparativos e da tonelagem V6 quando sua convenção não está confirmada.
- Manifesto e service worker para instalação e cache offline em HTTPS.

## Publicação no repositório existente

1. Antes da atualização, exporte um JSON no app antigo e confirme que o arquivo foi salvo.
2. Publique TODOS os arquivos da raiz deste pacote na pasta utilizada pelo GitHub Pages: index.html, app.js, engine.js, style.css, sw.js, manifest.webmanifest e os dois PNGs. A pasta tests e este LEIA-ME são documentação opcional.
3. Preserve o endereço e o caminho atuais. O armazenamento pertence à origem do navegador; mudar de domínio não leva os registros consigo.
4. Aguarde o deploy do GitHub Pages. Feche todas as abas e a versão instalada do app, depois reabra online. Um service worker antigo pode manter a tela antiga até ser substituído e todas as abas antigas serem fechadas.
5. Confirme “Training OS V6.0.0” no rodapé. Em Dados, aguarde “Pronto para abrir sem internet”. Não apague os dados do Safari para forçar uma atualização.
6. Se necessário, importe o JSON antigo pela aba Dados. Confira a prévia antes de substituir os registros atuais.

## Migração e comparabilidade

A chave antiga julio_apicelo_training_v4 não é apagada. A V6 usa julio_training_v6 e grava uma cópia estruturada da origem dentro dos dados migrados. Séries antigas marcadas sem quantidade/carga válidas deixam de contar, mas a entrada original permanece preservada. Pesagens duplicadas no mesmo dia são consolidadas no último valor, com a origem completa mantida no backup migrado.

O histórico antigo não é convertido automaticamente em histórico de novos movimentos. O hack continua chamado hack nos registros antigos. A fotografia de cada sessão garante que atualizações futuras da ficha não mudem o significado dos dados anteriores.

## Limites explícitos

- NÃO há conta, backend ou sincronização automática em nuvem. GitHub Pages hospeda os arquivos do app; não armazena seu histórico de treino. Transferência entre dispositivos é feita por JSON.
- Offline, comportamento com tela bloqueada, som e vibração precisam de validação no Safari real após publicação HTTPS. A prévia local não permite validar esse ciclo completo.
- RIR é uma estimativa do usuário, não uma medida automática. O campo pode ficar vazio. Em exercícios por tempo, deixe-o vazio se não fizer sentido para sua execução.
- Volume é carga externa registrada. Não mede hipertrofia. Assistência na barra fixa e peso corporal não entram na tonelagem. Halteres e séries por perna usam fator dois, conforme a convenção indicada.
- O app não decide aumento de carga nem altera a prescrição automaticamente.
- Uma sessão por tipo de treino por data. Outra sessão do mesmo tipo no mesmo dia reutiliza esse registro.
- Cópia de segurança LOCAL não substitui o arquivo JSON guardado fora do navegador. Há uma cópia local anterior; uma nova operação de substituição atualiza essa cópia.
- Exportar inicia o download. O app não consegue confirmar se o sistema operacional reteve o arquivo; confira no app Arquivos/Downloads.

## Verificações realizadas

14 testes automatizados passaram: volume e contagem, sessão vazia/futura, parcial/concluída, validação numérica, separação de equipamentos/unidades, migração do hack, cardio legado, descarte de tonelagem ambígua, estrutura de backup, round-trip JSON, CSV e datas/pesos inválidos.

No navegador: bloqueio de finalização vazia; registro de 60 kg × 8 reps = 480 kg × reps; sessão parcial; persistência após recarregar; pesagem com data própria; troca para prancha/segundos; exportação JSON e importação com prévia e cópia de segurança. Layout visual inspecionado em largura de 390 px. Dados de teste não estão incluídos neste pacote.

Para repetir os testes com Node.js: node --test tests/test-engine.js

A publicação no repositório não foi executada enquanto a conexão GitHub não estiver autorizada nesta conversa.
