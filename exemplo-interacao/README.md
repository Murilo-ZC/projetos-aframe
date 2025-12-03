# Exemplos de Interação com o AFrame

## cursor-olhar.html - Cursor que Acompanha o Olhar

Este exemplo demonstra como criar um **cursor circular** (reticle) que acompanha a direção do olhar do usuário em uma cena A-Frame.

### Funcionalidades

- **Cursor Ring**: Um anel circular posicionado no centro da visão do usuário que funciona como ponteiro
- **Fuse Click**: Sistema de clique por "fusão" - ao olhar para um objeto por 1.5 segundos, o clique é acionado automaticamente
- **Feedback Visual**: 
  - O cursor muda de cor (branco → ciano) quando passa sobre objetos interativos
  - Os objetos aumentam de tamanho quando o cursor está sobre eles
  - Animação de "encolhimento" do cursor durante o tempo de fusão

### Objetos na Cena

| Objeto | Cor | Ação ao Clicar |
|--------|-----|----------------|
| Cubo | Rosa | Gira 360° |
| Esfera | Verde | Muda para amarelo |
| Cilindro | Azul | Pula para cima |
| Torus | Roxo | Rotação contínua |

### Como Funciona

1. O cursor é uma entidade `<a-entity>` com geometria de anel (`ring`) posicionada como filho da câmera
2. O componente `cursor` do A-Frame com `fuse: true` permite interação baseada no olhar
3. O `raycaster` é configurado para detectar apenas objetos com a classe `.interativo`
4. Animações são acionadas por eventos como `mouseenter`, `mouseleave` e `click`

### Uso

Abra o arquivo `cursor-olhar.html` no navegador e movimente a câmera (arrastar o mouse ou mover o dispositivo mobile) para apontar o cursor para os objetos.
