# Fika - A multiplayer mod for SPT

<details open>
    <summary>Table of Contents</summary>
    <ol>
        <li><a href="#o-que-é-fika">O que é Fika</a></li>
        <li><a href="#licença">Licença</a></li>
        <li>
            <a href="#pré-requisitos">Pré Requisitos</a>
            <ul>
                <li><a href="#hospeando">Hospeando</a></li>
                <li><a href="#cliente">Cliente</a></li>
            </ul>
        </li>
        <li><a href="#requerimento-de-hardware">Requiremento de Hardware</a></li>
        <li>
            <a href="#instalação">Instalação</a>
            <ul>
                <li><a href="#hospedar-usando-redirecionamento-de-porta">Hospedar usando Redirecionamento de Porta</a></li>
                <li><a href="#hospedar-usando-vpn">Hospedar usando VPN</a></li>
                <li><a href="#hospedar-usando-playit">Hospedar usando Playit.gg</a></li>
                <li><a href="#cliente-dedicado">Cliente Dedicado</a></li>
                <li><a href="#client-usando-redirecionamento-de-porta">Cliente usando Redirecionamento de Porta</a></li>
                <li><a href="#client-usando-vpn">Cliente usando VPN</a></li>
            </ul>
        </li>
        <li>
            <a href="#características-e-configurações">Características e Configurações</a>
            <ul>
                <li><a href="#características-e-como-fazer">Características & Como fazer</a></li>
                <li><a href="#configuração-do-cliente">Configuração do Cliente</a></li>
                <li><a href="#configuração-do-server">Configuração do Server</a></li>
            </ul>
        </li>
    </ol>
</details>

## O que é FIKA

**Fika** é um mod para **SPT**  que permite você jogar COOP com seus amigos. Utiliza uma conexão P2P-UDP para uma experiencia moderna e eficaz. Os objetivos principais do Fika são: desempenho, precisão e suporte a mods. Fika atualmente é mantida pela Equipe Fika.
Junte-se ao nosso Discord [aqui](https://discord.gg/project-fika)!

## Licença

<img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by-nc-sa.png" alt="cc by-nc-sa" width="196" height="62" style="float:right">

Este projeto está licenciado sob [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/legalcode.en).

- Você só pode compartilhar/criar derivativos de Fika desde que sejam dados os devidos créditos e que não seja usado para fins comerciais.
- Você não pode monetizar seu servidor em termos de pagamentos ou doações.
- Você não pode hospedar servidores públicos em larga escala, Fika é destinado para COOP com seus amigos.
- Você não pode usar os **recursos artísticos** de Fika que são feitos à mão por nossos desenvolvedores e artistas sem a permissão do criador.

## Pré Requisitos

Fika requer conhecimento geral de computadores, redes e SPT. Se você não se sentir à vontade com esses conceitos, este projeto não é para você. Por favor, tente entender e respeitar isso.

### Hosteando

- Roteador e Provedora de Serviço que suporte **Redirecionamento de Porta** ou **UPnP**.
- Porta TCP 6969 aberta para o servidor SPT.
- Porta UDP aberta para tráfego P2P, padrão 25565. (se estiver usando UPnP, não é necessário)
- SPT instalado e funcionando, compatível com a versão do Fika que você vai usar.
- Acesso ao Firewall do Windows.
- Recomenda-se uma velocidade de internet de pelo menos 20 Mbit/s de upload e download. Cada cliente consome em média cerca de 400 kbit/s.

Se não conseguir redirecionar portas, você pode usar VPN como `ZeroTier` ou `Radmin` ou um proxy como ``Playit.gg``.

### Cliente

- Roteador e Provedora de Serviço que suporte **Redirecionamento de Porta** ou **UPnP**. | **NOTA**: Apenas necessario se irá hospedar dentro do jogo.
- Porta UDP aberta para tráfego P2P, padrão 25565. (se estiver usando UPnP, não é necessário) | **NOTA**: Mesma coisa que acima.
- SPT instalado e funcionando, compatível com a versão do Fika que você vai usar.
- Acesso ao Firewall do Windows.
- Recomenda-se uma velocidade de internet de pelo menos 20 Mbit/s de upload e download.

### Ambos

- A ultima versão dos arquivos Fika

## Requerimento de Hardware

Essas são as recomendações para uma experiência suave:

- **CPU**: i7 8700k / Ryzen 7 2700x
- **GPU**: GTX 1060 / RX 580
- **Memória** 16 GB mínimo, 32 GB altamente recomendado
- **Armazenamento**: SSD é obrigatório, não espere suporte se estiver rodando Fika em um HDD

Essas são as recomendações para um cliente dedicado:

- **CPU**: >4 GHz por núcleo
- **Memória**: >16 GB, 32 GB altamente recomendado
- **Armazenamento**: SSD é obrigatório

O maior ganho no Fika (e no SPT em geral) vai ser ter um CPU forte e mais RAM.

## Instalação

### Hospedar usando Redirecionamento de Porta

Antes de iniciar estas etapas, certifique-se de que você redirecionou todas as portas necessárias nas Pré-requisitos. Não iremos ajudá-lo a abrir suas portas. Se você não tiver acesso ao seu roteador ou não puder redirecionar portas, use uma VPN.

**Configuração do Firewall**

1. Redirecione a porta **TCP** 6969 no seu roteador (ambos entrada e saída)
2. Redirecione a porta **UDP** que você vai usar no seu roteador, padrão 25565 (ambos entrada e saída)
3. Quando solicitado pelo Windows, permita **todas** as conexões no seu Firewall
4. Se você ainda estiver tendo problemas, sugerimos que permita `EscapeFromTarkov.exe` (para todos) e `SPT.Server.exe` (host do servidor) para conexões de entrada e saída no Firewall Avançado do Windows.

**Configuração Geral**

1. [Baixe o plugin Fika mais recente](https://github.com/project-fika/Fika-Plugin/releases/latest) e [baixe o mod de servidor Fika mais recente](https://github.com/project-fika/Fika-Server/releases/latest)
2. Inicie o `SPT.Server.exe` uma vez para permitir que ele gere os arquivos de configuração para o Fika, depois feche-o novamente
3. Volte para a pasta principal e navegue até `SPT_Data\Server\configs` e abra `http.json`
4. Altere **ip** para `0.0.0.0` e **backendIp** para seu [IP WAN](https://ipv4.icanhazip.com/), depois salve o arquivo e feche-o
5. Navegue até `user\mods\fika-server\assets\configs` e abra `fika.jsonc`
6. Altere qualquer uma das configurações de acordo com suas preferências:
    - **useBtr**: se o BTR deve aparecer ou não ao jogar Streets
    - **friendlyFire**: se o fogo amigo deve ser ativado ou não
    - **dynamicVExfils**: ajusta automaticamente o número máximo de jogadores em veículos de exfiltração de acordo com a quantidade de jogadores na incursão
    - **allowFreeCam**: permite que os jogadores ativem a câmera livre durante as incursões
    - **giftedItemsLoseFIR**: se os itens enviados devem perder seu status FiR
7. Inicie o `SPT.Server.exe` e espere ele terminar de carregar
    - Isso é o que deve aparecer se ele tiver iniciado com sucesso, usando como exemplo o IP WAN `70.60.150.90`:
    ```
    Iniciado webserver em http://70.60.150.90:6969
    Iniciado websocket em ws://70.60.150.90:6969
    Servidor está rodando, não feche enquanto estiver jogando SPT, Bom jogo!!
    ```
8. Inicie `SPT.Launcher.exe`
9. Seus amigos podem se conectar utilizando seu WAN IP, que pode ser encontrado usando o site [IPv4.ICanHazIP](https://ipv4.icanhazip.com/)

### Hospedar usando VPN

Você precisa de uma VPN como `ZeroTier` ou `Radmin`. 

1. [Baixe o plugin Fika mais recente](https://github.com/project-fika/Fika-Plugin/releases/latest) e [baixe o mod de servidor Fika mais recente](https://github.com/project-fika/Fika-Server/releases/latest)
2. Navegue até a instalação do SPT e extraia o conteúdo do arquivo na pasta
3. Inicie o `SPT.Server.exe` uma vez para permitir que ele gere os arquivos de configuração para o Fika, depois feche-o novamente
4. Volte para a pasta principal e navegue até `SPT_Data\Server\configs` e abra `http.json`
5. Altere `ip` e `backendIp` para o IP da sua VPN, depois salve o arquivo e feche-o

Exemplo com um endereço fictício (**20.20.56.73**):
```json
{
    "ip": "20.20.56.73",
    "port": 6969,
    "backendIp": "20.20.56.73",
    "backendPort": 6969,
    "webSocketPingDelayMs": 90000,
    "logRequests": true,
    "serverImagePathOverride": {}
}
```
6. Navegue até `user\mods\fika-server\assets\configs` e abra `fika.jsonc`
7. Altere qualquer uma das configurações de acordo com suas preferências.
    - **useBtr**: se o BTR deve aparecer ou não ao jogar Streets
    - **friendlyFire**: se o fogo amigo deve ser ativado ou não
    - **dynamicVExfils**: ajusta automaticamente o número máximo de jogadores em veículos de exfiltração de acordo com a quantidade de jogadores na incursão
    - **allowFreeCam**: permite que os jogadores ativem a câmera livre durante as incursões
    - **giftedItemsLoseFIR**: se os itens enviados devem perder seu status FiR
8. Inicie o `SPT.Server.exe` e espere ele terminar de carregar
    - Isso é o que deve aparecer se ele tiver iniciado com sucesso, usando o IP de exemplo na etapa 5:
    ```
    Iniciado webserver em http://70.60.150.90:6969
    Iniciado websocket em ws://70.60.150.90:6969
    Servidor está rodando, não feche enquanto estiver jogando SPT, Bom jogo!!
    ```
9. Inicie o `SPT.Launcher.exe` e clique em 'Configurações'
10. No campo `URL`, altere para refletir o IP da sua VPN. Usando o exemplo na etapa 5, seria: `http://20.20.56.73:6969` (lembre-se de remover qualquer barra `/` no final)
11. Inicie o jogo e, após criar sua conta, defina tanto `Force IP` quanto `Force Bind IP` para o seu próprio IP pessoal da VPN. Você pode encontrar esses valores clicando em `F12` no menu principal.

### Hospedagem usando Playit

[Playit.gg](https://playit.gg/) é um proxy que torna possível hospedar servidores sem precisar redirecionar portas, 
encaminhando o tráfego do jogo por meio de um dos seus datacenters.
[Este guia](https://discuss.playit.gg/t/setup-an-escape-from-tarkov-multiplayer-server-with-spt-fika/3352) vai te ensinar como usar o Playit.gg
para hospedar um servidor SPT/Fika.
Editar seu ``http.json`` não é necessário.

### Cliente Dedicado

⛔ **Essa seção é apenas para usuários avançados** ⛔
1. Tenha certeza que você tem um servidor e cliente funcional instalado
2. Copie o cliente para uma nova pasta e instale a ultima versão do [plugin dedicado](https://github.com/project-fika/Fika-Dedicated/releases)
3. No seu `SPT.Server`, abra o arquivo de configuração `fika.jsonc` e no fim altere suas configurações do dedicado
```json
"dedicated": {
        "profiles": {
            "amount": 1 // a quantidade de perfis dedicados para ser gerado automaticamente, um por cliente dedicado
        },
        "scripts": {
            "generate": true, // se o script de startup deveria ser automaticamente gerado (necessario a menos que você saiba o que está fazendo)
            "forceIp": "127.0.0.1" // o ip que o cliente dedicado deveria se conectar, deixe padrão se for local
        }
    }
```
4. Inicie seu `SPT.Server` uma vez e deixe gerar o perfil e script de inicialização, então vá para `\user\mods\fika-server\assets\scripts` e encontre o script gerado. Mova isso para sua pasta raiz de instalação do Cliente criada na etapa 2 (se deseja re-gerar esses scripts, você precisa deletar o *antigo perfil dedicado*)
5. Redirecione a porta ou configure sua VPN normalmente, então mude manualmente a configuração do seu `fika.core` no `\BepInEx\config\com.fika.core.cfg`. Defina sua porta para a porta redirecionada, ou defina `set bind` e `force IP` para o IP do cliente dedicado.
6. Abra o cliente dedicado executando o script em lote (.bat), então no jogo quando estiver hospedando no seu próprio cliente, marque a opção "Usar Dedicado" para usar o cliente dedicado para hospedar. Só pode ser hospedado uma incursão por cliente. Geralmente é recomendado colocar todos os seus mods de IA no cliente dedicado e remover eles localmente, já que o cliente dedicado agora irá lidar com a IA.
O cliente dedicado roda em uma taxa de atualização de 60 FPS. Se quiser aumentar para um numero maior, insira `-updateRate=X` onde X é o a taxa de atualização desejada (max 120) no script de inicialização. Um exemplo seria:
```bat
-batchmode -nographics --enable-console true -updateRate=120 & exit
```
Mantenha em mente que um hardware forte é necessario para manter maiores taxas de atualização e o ganho é quase nulo.

⚠️ **NOTA**: Atualmente há inconsistencias com a mira da IA ao utilizar o cliente dedicado sem gráficos. Se possui uma maquina que está rodando, poderá tentar remover `-nographics` e até mesmo `-batchmode` para aliviar o problemam. Ainda estamos investigando soluçoes alternativas. ⚠️

### Cliente usando Redirecionamento de Porta

1. [Baixe a ultima versão do plugin Fika](https://github.com/project-fika/Fika-Plugin/releases/latest)
2. Navegue para sua instalação do SPT e extraia os conteúdos dos arquivos na pasta.
3. Inicie o `SPT.Launcher.exe` e selecione 'Configurações'
4. No campo `URL`, mude para refletir o WAN IP do host. Por exemplo, seria: `http://20.20.56.73:6969` (lembre-se de remover qualquer barra `/` no final)
5. Se hospedar no jogo, permita todas as conexõess (publicas and privadas) quando solicitado pelo Windows Firewall

### Client using a VPN

1. [Baixe a ultima versão do plugin Fika](https://github.com/project-fika/Fika-Plugin/releases/latest)
2. Navegue para sua instalação do SPT e extraia os conteúdos dos arquivos na pasta.
3. Inicie o `SPT.Launcher.exe` e selecione 'Configurações'
4. No campo `URL`, mude para refletir o VPN IP do host. Por exemplo, seria: `http://20.20.56.73:6969` (lembre-se de remover qualquer barra `/` no final)
5. Se hospedar no jogo, permita todas as conexõess (publicas and privadas) quando solicitado pelo Windows Firewall

## Características e Configurações

### Características & Como fazer
**Fika** permite que você hospede sessões P2P com seus amigos para jogar COOP. O host é quem controla a maioria da logica enquanto joga, tal como controle de IA, campos minados, zonas de sniper, o BTR, etc. Cada cliente é responsavel pelo seu próprio dano, ambos deles e da IA. Isso significa que atirar na IA é responsivo e rápido.

Para hospedar um jogo, selecione um mapa e horário, e então na tela final selecione `Hospedar Incursão`. Selecione a quantidade de jogadores que irão jogar (incluindo você mesmo) e espere carregar. Assim que estiver pronto, outras pessoas poderão se juntar a sua sessão, e quando todo mundo terminar de carregar, começará automaticamente.

**Outras caracteristicas de Fika**
- Enviar Itens
    - Com o botão direito do Mouse, clique em um item em seu inventário para mandar para outra conta
    - Pode ser customizado no [server](#configuração-do-server)
- Camera Livre (padrão tecla `F9`)
    - Na camera livre você pode teletortar para a posição da camera pressionando `T`
    - Você pode pular para outro jogador pressionando o clique `Esquerdo/Direito`
    - Você pode se fixar na cabeça de alguém segurando `ESPAÇO` quando pulando
    - Você pode se fixar nas costas de alguém, camera em terceira pessoa, segurando `CTRL` quando pulando
    - Você pode apertar `HOME` para ativar/desativar os controles da Camera Livre
- Multiplicadores de dano para areas cruciais em si mesmo
- Ia Dinamica para Host, no qual desabilita a IA quando ningúem está perto
- Limites customizados de IA por mapa
- Sistema de Triagem para aumentar desempenho
- Notificações personalizadas (colega morreu, chefe morreu para player, etc.)
- Sistema de Ping para marcar uma área no jogo para seus colegas
- Barras de vida para seus colegas
- Progresso de Missões compartilhadas na Incursão
- Cliente Dedicado

A maioria dessas caracteristicas podem ser configuradas na [configuração do cliente](#configuração-do-cliente).

### Configuração do Cliente

Para abrir a configuração do seu cliente, pressione a tecla `F12` no jogo. Vá para a seção `Fika Core` para configurar.

**Coop**

- **Mostrar Notificaçoes**: Habilita notificações personalizadas quando um jogador morre, extrai, mata um chefe, etc.
- **Auto Extrair**: Automaticamente extrai quando jogando como cliente, em vez de entrar na camera livre.
- **Mostrar Mensagem de Extração**: Se mostra a mensagem de extração após morrer/extrair.
- **Tecla de Extração**: A tecla usada para extrair da incursão.
- **Tecla do Chat**: A tecla usada para abrir a janela de chat.

**Coop | Personalizado**

- **Mostrar Placas de Nome dos Jogadores**: Alterna entre barras de vida e nomes.
- **Ocultar Barra de Vida**: Oculta completamente a barra de vida.
- **Mostrar HP% em vez da barra**: Mostra a vida em % em vez de usar a barra.
- **Mostrar Ícone de Facção do Jogador**: Exibe o ícone da facção do jogador ao lado da barra de vida.
- **Ocultar Placa de Nome ao Mirar**: Oculta a placa de nome ao visualizar através de miras PiP.
- **Placas de Nome Usam Zoom Óptico**:  A localização da placa de nome deve ser exibida usando a câmera óptica PiP.
- **Diminuir Opacidade na Periférica**: Diminui a opacidade das placas de nome quando não estiver olhando diretamente para um jogador.
- **Escala da Placa de Nome**: Tamanho das placas de nome.
- **Opacidade ao Mirar**: A opacidade das placas de nome ao mirar.
- **Sistema de Ping**: Alterna o Sistema de Ping. Se ativado, você pode receber e enviar pings pressionando a tecla de ping.
- **Botão de Ping**: Botão usado para enviar pings.
- **Cor do Ping**: A cor dos seus pings quando exibidos para outros jogadores.
- **Tamanho do Ping**: O multiplicador do tamanho do ping.
- **Reproduzir Animação de Ping**: Reproduz a animação de apontar automaticamente ao enviar um ping. Pode interferir na jogabilidade.

**Coop | Compartilhamento de Missões**
- **Tipos de Missão**: Quais tipos de missão receber e enviar.

**Coop | Depuração**

- **Botão de Câmera Livre**: Botão usado para alternar a câmera livre.
- **Modo AZERTY**: Se a câmera livre deve usar teclas AZERTY para entrada.
- **Sobreposição de Teclas**: Uma sobreposição com todas as teclas de atalho da câmera livre deve ser exibida.

**Desempenho**

- **IA Dinâmica**: Usa o sistema de IA dinâmica, desativando a IA quando estão fora do alcance de qualquer jogador.
- **Alcance da IA Dinâmica**: A distância em que a IA será desativada dinamicamente.
- **Taxa de IA Dinâmica**: Com que frequência a IA dinâmica deve escanear o alcance de todos os jogadores.

**Desempenho | Máximo de Bots**

- **Limites de Geração Impostos**: Impõe limites de geração ao gerar bots, garantindo que não ultrapassem os limites padrão. Isso afeta principalmente quando se usa mods de geração ou algo que modifique os limites de bots.
- **Despawn Furthest**: Ao impor limites de geração, o bot mais distante deve ser removido em vez de bloquear a geração. Isso tornará o ataque muito mais ativo em uma contagem menor de Máximo de Bots. Útil para PCs mais fracos. Só removerá pmcs e scavs. Se você não usar um mod de geração dinâmica, isso, no entanto, esgotará rapidamente as gerações no mapa, tornando o ataque muito morto em vez disso.
- **Despawn Minimum Distance**: Não remova bots dentro desta distância.
- **Máximo de Bots** `MAP`: Quantidade máxima de bots que podem estar ativos ao mesmo tempo no MAP. Útil se você tiver um PC mais fraco. Defina para 0 para desativar.

**Rede**

- **Soquete Nativo**:  Soquete Nativo para trafego de gameplay. Isso utiliza chamadas diretas no soquete para enviar/receber, aumentando drasticamente a velocidade e reduzindo a pressão do GC. Apenas para Windows/Linux e talvez nem sempre funcione.
- **Forçar IP**: Força o servidor quando hospedando a usar este IP ao transmitir para o backend em vez de automaticamente tentar pegar ele. Deixe vazio para desativar. Isso é obrigatorio quando usando uma VPN, utilize seu VPN IP pessoal.
- **Forçar Bind IP**: Força o servidor quando hospedando a utilizar este IP local quando iniciado o servidor. Deixe vazio para desativar. Isso é obrigatorio quando usando uma VPN, utilize seu VPN IP pessoal.
- **Porta UDP**: Porta a usar para pacotes UDP de gameplay.
- **Usar UPnP**: Tenta abrir portas utilizando UPnP. Util se você não conseguir abrir portar mas seu roteador suporta UPnP.
- **Usar NAT Punching**: Use NAT punching quando hospedar uma incursão. Apenas funciona com roteadores com NAT tipo Cone Completo (fullcone) e requer NatPunchServer habilitado no server SPT. UPnP, Forçar IP e Forçar Bind IP estão desabilitados neste modo.
- **Tempo para Esgotar a Conexão**: Quanto tempo leva para a conexão ser considereada descartada se nenhum pacote ser recebido.

**Gameplay**

- **Multiplicador de Dano a Cabeça**: Multiplicador X ao dano recebido na cabeça. 0.2 = 20%
- **Multiplicador de Dano a Axila**: Multiplicador X ao dano recebido na axila. 0.2 = 20%
- **Multiplicador de Dano a Estômago**: Multiplicador X ao dano recebido no estômago. 0.2 = 20%
- **Desabilitar Metabolisto em Bot**: Desabilita metabolismo em bots, prevenindo de morrerem de perda de energia/hidratação durante incursões longas.

### Configuração do Server

A configuração de servidor pode ser encontrado na pasta `user\mods\fika-server\assets\configs` . Abra `fika.jsonc` com um editor de texto.

```json
{
    "client": {
        "useBtr": true, // se o BTR deve aparecer ou não ao jogar Streets, padrão: true
        "friendlyFire": true, // se o fogo amigo deve ser ativado ou não, padrão: true
        "dynamicVExfils": false, // se o veículo de extração devera escalar com a quantidade de jogadores em incursão, diferente do padrão de 4, padrão: false
        "allowFreeCam": false, // se a camera livre pode ser ativada livremente, padrão: false
        "allowItemSending": true, // se enviar itens deveria estar ativo, padrão: true
        "blacklistedItems": [], // IDs de items que não podem ser enviados, e.g. ["5c94bbff86f7747ee735c08f", "5c1d0f4986f7744bb01837fa"] não permitiria jogadores de enviar cartões de acesso e o cartão o cartão preto
        "forceSaveOnDeath": false, // se o salvamento de perfil é forçado na morte, prevenindo o esquema de dar ALT+F4 para manter os itens ao morrer, padrão: false
        "mods": {
            "required": [], // mods necessarios no servidor, se habilitado sempre deve incluir os mods padrões do SPT: ["com.SPT.custom", "com.SPT.singleplayer", "com.SPT.core", "com.SPT.debugging", "com.fika.core", "com.bepis.bepinex.configurationmanager"]
            "optional": [] // mods que são permitidos fora dos necessarios
        },
        "useInertia": true, // se inércia deveria estar habilitada, padrão: true
        "sharedQuestProgression": false // se a progressão de missões em incursão devem ser compartilhadas, padrão: false
    },
    "server": {
        "giftedItemsLoseFIR": true, // se itens enviados dever perder seu status de FiR, padrão: true
        "launcherListAllProfiles": false, // se o launcher deve permitir mostrar todos os perfis, padrão: false
        "sessionTimeout": 5, // quanto tempo o servidor espera por um ping do cliente até a sessão ser considerada quebrada, padrão: 5
        "showDevProfile": false, // se perfis DEV podem ser criados, padrão: false
        "showNonStandardProfile": false // se perfis que não são padrão do EFT podem ser criados, padrão: false
    },
    "natPunchServer": {
        "enable": false, // se nat punching deveria estar habilitado: false
        "port": 6970, // porta para nat punching, padrão: 6970
        "natIntroduceAmount": 1
    }
}
```
