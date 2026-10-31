# Julio Training OS V6.2.0

Atualização de 31/10/2026 para o aplicativo publicado em:
https://sebpitstoprog.github.io/julio-training-os./index.html

## Divisão semanal

- Segunda: PUSH + abdômen, 19 séries.
- Terça: LEGS A, 17 séries.
- Quarta: PULL, 16 séries.
- Quinta: cardio leve de 20–30 minutos + abdômen, 3 séries.
- Sexta: LOWER B, 18 séries.
- Sábado: UPPER complementar, 16 séries.
- Domingo: descanso.

Total: 89 séries-base semanais, incluindo panturrilhas e abdômen. Séries de aquecimento não entram nessa contagem.

## Fichas

### PUSH

- Supino reto com barra: 3×6–8.
- Supino inclinado com halteres: 3×8–12.
- Crucifixo no cabo ou voador: 3×10–15.
- Desenvolvimento com halteres sentado: 2×8–12.
- Elevação lateral: 3×12–20.
- Tríceps corda na polia: 3×10–15.
- Abdominal no solo: 2×12–20.

### LEGS A

- Agachamento livre: 3×6–10.
- Leg press 45°: 3×10–15.
- Cadeira extensora: 3×10–15.
- Mesa flexora: 3×10–15.
- Cadeira adutora: 2×12–20.
- Panturrilha em pé: 3×10–15.

### PULL

- Puxada alta pela frente, pegada neutra: 3×8–12.
- Remada na máquina com peito apoiado: 3×8–12.
- Pulldown com braços quase estendidos: 2×12–15.
- Voador inverso: 3×12–20.
- Rosca com halteres no banco inclinado: 3×8–12.
- Rosca Scott na máquina ou com barra EZ: 2×10–15.

### CARDIO + CORE

- Cardio leve: 20–30 minutos em ritmo confortável.
- Abdominal no solo: 3×12–20.

### LOWER B

- Elevação pélvica com barra ou máquina: 3×8–12.
- Levantamento romeno: 3×8–10.
- Agachamento búlgaro com apoio: 3×8–12 por perna.
- Cadeira flexora: 3×10–15.
- Cadeira abdutora: 3×12–20.
- Panturrilha sentado: 3×12–20.

### UPPER complementar

- Supino inclinado com halteres: 3×8–12.
- Remada na máquina com peito apoiado: 3×8–12.
- Puxada alta pela frente, pegada neutra: 2×10–15.
- Elevação lateral: 3×12–20.
- Tríceps acima da cabeça no cabo: 3×10–15.
- Rosca martelo: 2×10–15.

## Execução e progressão

- Agachamento, romeno e búlgaro: aproximadamente 2 repetições em reserva.
- Demais exercícios: 1–2 repetições em reserva.
- Exercícios compostos: descanso de 2–3 minutos.
- Isoladores: descanso de 90–120 segundos.
- Abdômen: descanso de 60–90 segundos, sem carga externa obrigatória.
- Ao alcançar o teto da faixa em todas as séries, com execução estável e o RIR previsto, aumentar pelo menor incremento disponível.
- O bloco foi planejado para 6–8 semanas, com revisão de desempenho a cada duas semanas.
- Drop-set e rest-pause não são obrigatórios neste bloco.

## Proteção do histórico

- Sessões antigas continuam com a ficha original salva.
- Sessões novas usam a revisão 3, identificada como V6.2.
- Para trocar uma sessão já criada, usar “Trocar para ficha V6.2”. O aplicativo cria antes uma cópia local de segurança.
- O armazenamento continua local no navegador. Exportar o backup JSON regularmente.
- Não apagar os dados do Safari para forçar atualização.

## Publicação no GitHub Pages

1. Exportar um backup JSON antes da atualização.
2. Enviar para a raiz do repositório: `index.html`, `app.js`, `engine.js`, `style.css`, `sw.js`, `manifest.webmanifest`, `icon-192.png` e `icon-512.png`.
3. Confirmar o commit e aguardar o GitHub Pages concluir a publicação.
4. Fechar todas as abas do aplicativo e abrir novamente em uma aba normal do Safari.
5. Confirmar “Training OS V6.2.0” no rodapé.

`LEIA-ME.md` e a pasta `tests` são documentação e não precisam ser publicados.

## Verificações realizadas

- 17 testes automatizados passaram.
- Preservação de sessões V6.1 e registros legados validada.
- Cardio e abdômen podem ser salvos como sessão completa ou parcial.
- Interface V6.2 verificada no navegador.
- Registro completo de 25 minutos de cardio e 3 séries de abdômen testado.

Para repetir os testes:

```bash
node --test tests/test-engine.js
```

## Base científica usada na reorganização

- Pelland et al. Volume e hipertrofia com retornos decrescentes: https://pubmed.ncbi.nlm.nih.gov/41343037/
- Schoenfeld et al. Frequência sem vantagem clara quando o volume é igualado: https://pubmed.ncbi.nlm.nih.gov/30558493/
- Nunes et al. Ordem dos exercícios e prioridade de força: https://pubmed.ncbi.nlm.nih.gov/32077380/
- Refalo et al. Hipertrofia semelhante com 1–2 RIR versus falha em treinados: https://pubmed.ncbi.nlm.nih.gov/38393985/
- Plotkin et al. Agachamento e elevação pélvica para glúteos: https://pubmed.ncbi.nlm.nih.gov/37877099/

Esses estudos sustentam princípios gerais. Eles não determinam individualmente a dose ideal. O ajuste depende da progressão, execução e recuperação registradas ao longo do bloco.
