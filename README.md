# 🎸 App Inventor Strumming Pad  
Um simulador de “strum” criado com **MIT App Inventor**, onde o usuário toca ou arrasta o dedo sobre um Canvas dividido em 10 faixas sonoras, cada uma reproduzindo uma nota.  
O projeto implementa **polifonia, pré-carregamento de áudio, otimização do arraste (drag)** e divisão visual do canvas.

---

## 📱 Funcionalidades
- 🎵 **10 notas independentes**, divididas verticalmente no Canvas  
- 🎹 **Polifonia realista** usando múltiplos componentes Sound  
- ⚡ **Baixa latência** graças a pré-carregamento inteligente  
- 🎨 **Canvas com divisões visuais** desenhadas automaticamente  
- 🖐️ **Toque responsivo (tap) e arraste suave (drag)**  
- 💡 Toca a nota **somente quando o dedo muda de segmento**, evitando repetição e lag  
- 🔊 Compatível com WAV para melhor desempenho

---

## 🧠 Estrutura da Lógica
### 1. Divisão do Canvas
No `Screen.Initialize`, o app:
- Calcula a altura de cada um dos 10 segmentos  
- Desenha 9 linhas horizontais para separar os espaços  
- Define cor e espessura das linhas  

### 2. Sistema de Polifonia
- Cria uma lista com vários componentes `Sound`  
- Usa um índice circular para escolher sempre o próximo sound livre  
- Preenche o `.Source` previamente para reduzir delay  

### 3. Strum Inteligente
Durante o arraste:
- Detecta o segmento pela posição Y do dedo  
- Toca somente se o índice mudou  
- Evita centenas de chamadas por segundo  
- Mantém fluidez e remove distorção sonora  

---

## 🚀 Instalação e Uso
1. Abra o **MIT App Inventor**  
2. Importe o arquivo `.aia` (se estiver incluído neste repositório)  
3. Adicione seus arquivos de áudio na pasta "Assets"  
4. Conecte o app via Companion ou gere o APK  
5. Execute no celular:

- Toque em qualquer faixa → nota individual  
- Arraste do topo para baixo → efeito de strum  

---


---

## 🔧 Customização
Você pode alterar facilmente:
- Quantidade de segmentos  
- Mapeamento das notas  
- Cores e espessuras das divisões  
- Sons (WAV recomendado)  
- Comportamento no arraste  

---

## 🧪 Tecnologias
- MIT App Inventor  
- Componentes Sound  
- Canvas API  
- Lógica de eventos (Touched / Dragged)

---

## 📝 Licença
Este projeto está sob a licença **MIT**.  
Sinta-se livre para alterar e distribuir.

---

## ❤️ Contribuição
Pull Requests são bem-vindos!  
Sugestões, melhorias e otimizações de performance podem ser abertas como Issues.

---

## 📩 Contato
Dúvidas, ideias ou melhorias?  
Abra uma Issue no repositório ou entre em contato diretamente.

