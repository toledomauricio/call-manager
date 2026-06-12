# Política de Privacidade — Call Organizer

_Última atualização: 12 de junho de 2026_

A extensão **Call Organizer** foi desenhada com privacidade em primeiro lugar.

## Resumo

- **Nenhum dado é coletado, transmitido ou compartilhado.**
- **Não há servidor/backend.** Tudo funciona localmente no seu navegador.
- A extensão **não grava, não escuta e não armazena o áudio** das suas ligações.

## Que dados a extensão manipula

Todos os dados abaixo ficam **exclusivamente no seu dispositivo**, armazenados no
`IndexedDB` e no `chrome.storage` do próprio navegador:

- Cadastro de **colaboradores** (nome e a marcação de "quem sou eu");
- Cadastro de **clientes** e **agendamentos** que você criar;
- **Histórico de ligações**: data/hora de início e fim e a duração de cada ligação,
  além da contagem diária por colaborador.

## Como a detecção de ligações funciona

A extensão instala um "gancho" nas APIs `getUserMedia` e `RTCPeerConnection` da
página do seu discador web. Esse gancho serve **apenas** para saber **quando** uma
faixa de áudio é aberta e fechada (início e fim de uma ligação), permitindo contar
e cronometrar as chamadas.

A extensão **não acessa o conteúdo do áudio**, **não o grava** e **não o envia** para
lugar nenhum.

## Permissões solicitadas

- **`storage`** — guardar localmente os dados acima.
- **`contextMenus`** — atalhos no menu de contexto do navegador.
- **Acesso aos sites (`content_scripts` em todas as URLs)** — necessário para detectar
  o início/fim das ligações em qualquer discador web que você utilizar. Nenhuma
  informação da página é lida, coletada ou transmitida.

A extensão **não** solicita permissões de rede, histórico, cookies ou dados de
navegação.

## Compartilhamento de dados

Nenhum. Como não há transmissão de dados, nada é compartilhado com terceiros.

## Exclusão de dados

Você pode apagar os dados a qualquer momento removendo registros pelo painel ou
desinstalando a extensão (o que limpa todo o armazenamento local).

## Contato

Em caso de dúvidas sobre esta política, entre em contato com o desenvolvedor pelo
e-mail informado na página da extensão na Chrome Web Store.
