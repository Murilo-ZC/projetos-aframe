# Projetos com AFrame

Repositório criado para criar projetos com a biblioteca AFrame. Sua documentação pode ser encontrada [aqui](https://aframe.io/). Mais detalhes sobre o projeto podem ser vistos no site do projeto. Aqui vamos colocar nossas energias em utlizar essa ferramenta e como podemos utilizar ela com projetos de AR (Realidade Aumentada) e VR (Realidade Virtual).

## Por que aplicações WebVR precisam de HTTPS?

Aplicações WebVR exigem o uso de HTTPS devido a políticas de segurança implementadas pelos navegadores modernos. Essas políticas restringem o acesso a recursos sensíveis, como sensores de movimento, APIs de realidade virtual e dispositivos de entrada (como controles VR), apenas a contextos considerados **seguros** (secure contexts), ou seja, aqueles servidos por HTTPS.

### Requisitos de Segurança

1. **APIs Sensíveis**: As APIs WebVR e WebXR acessam recursos do sistema como:
   - Sensores de movimento e orientação do dispositivo
   - Câmeras e microfones
   - Dispositivos de entrada VR/AR
   - Dados de posicionamento espacial

2. **Políticas dos Navegadores**: Navegadores modernos (Chrome, Firefox, Safari, Edge) implementam a política de **Secure Contexts**, que exige HTTPS para:
   - Proteger dados do usuário contra interceptação
   - Prevenir ataques man-in-the-middle
   - Garantir integridade da comunicação entre cliente e servidor

3. **Experiência do Usuário**: Sem HTTPS, as aplicações WebVR simplesmente não funcionarão corretamente, pois as APIs necessárias estarão bloqueadas ou indisponíveis.

### Caddy: Uma Solução 

O [**Caddy**](https://caddyserver.com/) é um servidor web moderno que facilita significativamente a implementação de HTTPS para aplicações WebVR, oferecendo:

#### HTTPS Automático
- Obtém e renova certificados SSL/TLS automaticamente via **Let's Encrypt**
- Elimina a necessidade de configurações manuais complexas
- Funciona tanto em produção quanto em desenvolvimento local

#### Configuração Simplificada
- Sintaxe intuitiva no arquivo `Caddyfile`
- Configuração mínima necessária para começar
- Ideal para desenvolvimento rápido de aplicações WebVR

#### Performance e Modernidade
- Suporte nativo a **HTTP/2** e **HTTP/3** (QUIC)
- Melhor desempenho e tempos de carregamento mais rápidos
- Otimizado para aplicações web modernas

#### Proxy Reverso
- Facilita o roteamento de múltiplas aplicações
- Suporte a múltiplos domínios e subdomínios
- Configuração flexível para ambientes de desenvolvimento e produção

Ao utilizar o Caddy para servir aplicações WebVR, garantimos que elas operem em um ambiente seguro, atendendo às políticas de segurança dos navegadores e proporcionando uma experiência de usuário otimizada. A configuração automática de HTTPS elimina barreiras técnicas, permitindo que desenvolvedores se concentrem na criação de experiências imersivas em vez de configurações de servidor.

