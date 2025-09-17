# 📌 Introdução ao Arduino

O **Arduino** é uma plataforma de prototipagem eletrônica **open source** que combina **hardware e software** de fácil utilização.  
Ele permite criar projetos interativos usando **sensores, atuadores e programação** em C/C++ através da **IDE do Arduino**.  

A placa Arduino possui um **microcontrolador** (ex.: ATmega328) que pode ser programado via USB.  
É bastante usado em:  

- 🤖 Robótica  
- ⚡ Automação  
- 🌐 IoT (Internet das Coisas)  
- 🎓 Educação em eletrônica e programação  

---

## 🧾 Comentários no Código Arduino

Os comentários **não são executados** pelo microcontrolador. Eles servem para documentar e explicar o código.

```cpp
/**
 * Comentário de Cabeçalho
 * Explica objetivo, autor, data, licença, etc.
 */

/*
  Comentário em Bloco
  Usado para várias linhas ou para desativar partes do código.
*/

// Comentário em Linha
// Explica instruções individuais.


⚠️ Boas Práticas

✅ Use comentários para explicar o "porquê" do código
✅ Seja claro e objetivo
✅ Atualize os comentários quando modificar o código

❌ Evite comentários óbvios demais
❌ Não deixe comentários desatualizados ou confusos


💡 Projeto: Piscar LED

Exemplo clássico para iniciantes: fazer um LED no pino 13 piscar a cada 1 segundo.

/**
 * Exemplo: Piscar LED
 * Autor: Enzo Mesquita
 * Objetivo: Demonstrar uso de saídas digitais
 */
 
void setup() {
  pinMode(13, OUTPUT); // define o pino 13 como saída
}

void loop() {
  digitalWrite(13, HIGH); // acende o LED
  delay(1000);            // espera 1 segundo (1000 ms)
  digitalWrite(13, LOW);  // apaga o LED
  delay(1000);            // espera 1 segundo
}

🔧 Comandos Importantes

Comando	Função	Exemplo

pinMode(pino, OUTPUT)	Configura o pino como saída	pinMode(13, OUTPUT);
digitalWrite(pino, HIGH)	Envia 5V (liga o dispositivo)	digitalWrite(13, HIGH);
digitalWrite(pino, LOW)	Envia 0V (desliga o dispositivo)	digitalWrite(13, LOW);
delay(ms)	Pausa o programa em milissegundos	delay(1000); // 1 segundo



---

⏱️ Sobre o Delay

delay(1000) → 1 segundo

delay(500) → 0,5 segundo

delay(100) → 0,1 segundo


Quanto menor o valor, mais rápido o LED pisca.


---

🚀 Conclusão

O projeto Pisca LED é o primeiro passo no mundo Arduino, perfeito para aprender como controlar saídas digitais e entender a lógica básica de programação embarcada.⬇


# oo 📟 Relatório: Uso do Multímetro 

O **multímetro** é uma ferramenta eletrônica versátil, utilizada para medir diferentes grandezas elétricas em circuitos, como **tensão (V)**, **corrente (A)** e **resistência (Ω)**.  

---

## 🔌 Principais Entradas

- **COM** → borne de referência/terra (fio preto).  
- **V/mA/Ω** → entrada para medir tensão, corrente baixa e resistência (fio vermelho).  
- **10A/20A** → entrada exclusiva para correntes mais altas (dependendo do modelo).  

---

## 🧾 Símbolos Mais Usados

| Símbolo | Função |
|---------|--------|
| **V⎓ (DCV)** | Tensão contínua (pilhas e baterias) |
| **V∿ (ACV)** | Tensão alternada (tomadas/rede elétrica) |
| **A⎓ (DCA)** | Corrente contínua |
| **A∿ (ACA)** | Corrente alternada |
| **Ω** | Resistência elétrica |
| **🔔 (bip)** | Teste de continuidade |
| **→|– (diodo)** | Teste de diodos e semicondutores |

---

## ⚡ Medindo Tomadas (Tensão AC)

- Utilize a escala de **200V ou 600V** (nunca abaixo disso).  
- Em rede de **127V**, a leitura típica varia entre **121V e 123V**.  
- Em rede de **220V**, use a escala de **600V**.  
- ⚠️ **Atenção:** nunca encostar as pontas de prova entre si quando estiverem na tomada.  

---

## 🔋 Tipos de Tensão

- **Tensão Contínua (DC):**  
  - Tem lado positivo (+) e negativo (–).  
  - Usada em **baterias e pilhas**.  

- **Tensão Alternada (AC):**  
  - Não possui polaridade fixa.  
  - Usada em **tomadas e rede elétrica**.  

---

## 📊 Exemplos de Medição

- **Bateria 9V:** leitura típica próxima a **9V** (ex.: 9,69V).  
- **Pilha AA/AAA:** valor nominal de **1,5V**.  
- **Bateria da placa-mãe (CR2032):** especificação de **3V**.  
  - Sempre instalar com o **lado negativo para baixo**.  
  - Colocar invertida pode **danificar o slot**.  

---

## 🌀 Medindo Resistência (Ω)

- Usado para resistores e continuidade de cabos.  
- “1” ou “OL” = **não há continuidade**.  
- Se apitar no modo **🔔**, significa que há passagem de corrente (fio bom).  

---

## 🔍 Medindo Corrente (A)

- Corrente deve ser medida **em série** (o multímetro entra no circuito).  
- Verifique se vai usar a entrada **mA** ou **10A**.  
- ⚠️ **Nunca medir corrente direto na tomada!** Risco de queimar o multímetro.  

---

## 🛡️ Cuidados de Segurança

- Ponta **preta sempre no COM**.  
- Escolha a escala **acima do valor esperado**.  
- Não medir resistência em componentes energizados.  
- Não deixar o multímetro no modo **corrente** ao medir tensão.  
- Guardar em local seco, longe de umidade.  

---

## 📌 Guia Rápido de Escalas

| O que medir | Escala no multímetro |
|-------------|-----------------------|
| Tomada 127V | **200V AC** |
| Tomada 220V | **600V AC** |
| Pilha AA/AAA | **20V DC** |
| Bateria 9V | **20V DC** |
| Bateria placa-mãe 3V | **20V DC** |
| Resistores | **Ω (faixa adequada)** |
| Continuidade de cabos | **🔔 (bip)** |

---

## 📝 Observação Final

- Quando a **voltagem de pilhas/baterias começar a cair**, significa que estão descarregando.  
- Valores muito abaixo da especificação indicam que é hora de **trocar ou recarregar**.  
