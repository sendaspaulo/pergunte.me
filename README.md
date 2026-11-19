# pergunte.me

Uma skill em português para transformar pedidos de software em prompts que a equipe pode usar em agentes de programação. Ela identifica o projeto, esclarece uma decisão por vez e combina como verificar o resultado.

## Como usar

Com a skill instalada, peça **“faz um prompt pra mim”**. A primeira pergunta será **“Para qual projeto é esse prompt?”**. Se você já informou o projeto, a entrevista começa pela decisão que estiver em aberto.

Por exemplo, ao receber **“faz um prompt para corrigir a exportação de pedidos no ERP”**, a skill pode perguntar **“O que acontece hoje quando alguém tenta exportar os pedidos?”**.

Para receber o prompt imediatamente, diga **“pular perguntas”** ou **“é um teste pessoal e não um projeto”**. Os atalhos funcionam no início e no meio da entrevista.

## Exemplo completo: um CRUD para uma locadora de carros

> gere um prompt que seja um crud para um site de locação de carros

O projeto já está identificado. A primeira decisão é **qual cadastro construir**. Um cadastro de veículos identifica cada unidade pela placa. Um cadastro de reservas precisa relacionar cliente, veículo e período e tratar conflitos de datas.

### Como a entrevista evolui

Neste diálogo ilustrativo, a atendente representa a **Curva**, uma locadora fictícia. A skill faz uma pergunta por vez e usa cada resposta para escolher a próxima.

| Pergunta da pergunte.me | Resposta da atendente | O que muda no site |
| --- | --- | --- |
| Qual cadastro você quer gerenciar primeiro? | Os veículos. Temos vários carros do mesmo modelo. | Cada linha representa uma unidade identificada pela placa. |
| Quem usa o cadastro no dia a dia? | A atendente do balcão precisa informar a disponibilidade e a diária por telefone. | A lista mostra esses dados juntos e permite buscar por modelo ou placa. |
| Como você registra a situação de um carro? | Marco manualmente como disponível, locado ou em manutenção. | A edição atualiza os totais da frota. |
| O que deve acontecer ao excluir? | Quero conferir o modelo e a placa e poder cancelar. | A confirmação identifica o veículo antes de removê-lo. |
| Onde os dados precisam ficar salvos? | Para a demonstração, basta reabrir o mesmo navegador. | A frota é salva localmente. Cada navegador mantém sua cópia. |

### Do prompt ao site

Com o escopo confirmado, o prompt pede as quatro operações sobre veículos, placa única, diária positiva, busca combinada com filtro e persistência após recarregar. **O prompt completo, pronto para copiar, está na página 4 do PDF.**

No teste real, a tentativa de cadastrar `crv-1a01` foi bloqueada porque `CRV1A01` já existia. Um Honda City foi então cadastrado com a placa `TES2B30`, editado para **R$ 205,50** e colocado em manutenção. A consulta pela placa após recarregar mostrou os novos valores. Cancelar a exclusão preservou o carro. Confirmar a exclusão devolveu a frota aos seis veículos iniciais.

- [Ler o estudo de caso em PDF](exemplos/locadora/do-prompt-ao-site.pdf) — entrevista, decisões, prompt final e roteiro de teste em cinco páginas.
- [Abrir o código da demonstração](exemplos/locadora/index.html) — para testar, baixe o arquivo pelo botão **Download raw file** do GitHub e abra-o no navegador. O HTML já inclui os estilos e o JavaScript.

## Arquivos

As instruções ficam em [SKILL.md](SKILL.md). O nome exibido é **pergunte.me** e o identificador de instalação é **pergunte-me**.

Adaptada da [grill-me de Matt Pocock](https://github.com/mattpocock/skills). Consulte a [licença MIT](LICENSE).
