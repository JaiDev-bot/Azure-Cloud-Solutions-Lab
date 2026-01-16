# 🕵️‍♀️ Estudo de caso: aonde foi parar meu CPF e meu RG?

> **Status do experimento:** Concluído com sucesso (e uma leve indignação de uma boa patriota).

Neste módulo do laboratório, decidi testar os limites do **Azure AI Language**. O objetivo era simples: verificar se a IA é realmente o guardião da privacidade que a LGPD exige ou se ela só tirou o visto para o Hemisfério Norte.

---

##  O cenário:

Coloquei dois modelos de processamento de linguagem natural (NLP) frente a frente no **Azure AI Foundry** `(o queridinho da Microsoft) `:

1.  **NER (Extração de Entidades Nomeadas):** O "conhecido de todos". Ele foca em identificar que *algo* é um número, uma pessoa ou um lugar.
2.  **PII (Informações Identificativas):** O "segurança". Ele deveria ser o responsável por detectar e ocultar dados sensíveis para conformidade com leis como a **LGPD**.

---

## 📸 Prova A: O NER e o CPF brasileiro
O modelo de NER é aquele aluno esforçado. Ele olhou para o meu CPF e disse: "uuu, isso aqui é uma entidade importante!". Identificou nome, cidade e o número do CPF e RG em 2 segundos.

> O NER identificando o CPF e RG que o PII "esqueceu".
![Print gráfico](https://github.com/JaiDev-bot/Azure-Cloud-Solutions-Lab/blob/main/AZURE/%5BPII-EXTRACTION%5D%20pontos-cegos/NER.png)




---

## 📸 Prova B: O PII e a amnésia seletiva
Aqui é onde o parquinho do Azure pega fogo. Ao rodar o extrator de **PII**, a IA teve uma crise de identidade. Ela identificou o **Social Security Number (SSN)** do Jordan Smith (EUA) com uma precisão de dar inveja(é sério, fiquei com inveja), mas quando chegou no CPF br... o silêncio foi ensurdecedor. Para o PII, o meu CPF é apenas um ruído no sistema.


> *PII Extraction mostrando o sotaque americano rsrs.*
![Print PII EUA](https://github.com/JaiDev-bot/Azure-Cloud-Solutions-Lab/blob/main/AZURE/%5BPII-EXTRACTION%5D%20pontos-cegos/EUA.png)

---

> *PII Extraction fingindo que CPF é número de sorteio no instagram.*
![print PII br](https://github.com/JaiDev-bot/Azure-Cloud-Solutions-Lab/blob/main/AZURE/%5BPII-EXTRACTION%5D%20pontos-cegos/Jai.png)


---

##  LGPD, vem aqui, vamos conversar!

A ironia técnica é deliciosa, mas o perigo é real. Como podemos falar em conformidade e segurança se o serviço de "Informações Identificativas" da nuvem mais usada do mundo ignora o principal documento de identificação do Brasil?

* **O Risco:** Se uma empresa confia cegamente no PII do Azure para limpar logs ou anonimizar dados, ela está deixando CPFs e RGs vazarem livremente enquanto protege o seguro social de gringos que nem moram aqui.
* **A Falha de soberania:** A IA é treinada para o "Norte global". Se o seu dado não está no mapeamento oficial de Seattle, você é tecnicamente invisível para a segurança da plataforma.


# 💸 O preço da amnésia:

> A IA não conseguiu extrair o CPF nem o RG, mas o juiz consegue no processo!! rsrs

Vamos falar de valores reais, porque compliance não se faz com sorrisos:
* **A multa pesada:** Um CPF vazado em logs porque a IA não o mascarou pode gerar multas de **2% do faturamento bruto**, chegando até **R$ 50 milhões por infração**.
* **Dano à imagem:** Imagine explicar para o Board que os dados vazaram porque a IA "só falava inglês". O custo de perda de mercado é imensurável.
* **Inexistência de soberania brasileira:** Depender de um modelo treinado em Seattle para proteger um cidadão em SP é um risco estratégico que nenhuma empresa séria deveria correr.

# A Real 😈:

A real é que um vazamento de dados pode destruir empresas pequenas e apenas arranhar as grandonas. E nem vou entrar a fundo na reputação, porque aí ambas terão "probleminhas" de imagem que nenhum marketing resolve.

Se uma empresa pequena (ou um grupo de doidos da cabeça) decide subir um site sem lidar com a segurança de maneira rigorosa, o vazamento dessas informações pode custar o CNPJ.

**Imagine o cenário:** Você cria um site de relacionamentos e, do nada, um invasor passa pela sua segurança "de fábrica" e vaza conversas íntimas e documentos sigilosos.

> Eu juro que não é sobre o site que vazou informações de mulheres saficas, EU JURO!! (rsrs)


Agora faz a conta comigo:
* Imagine que cada pessoa inicie um processo e ganhe **R$ 2.000,00** (um valor "baixo" para danos morais). 
* Agora imagine que **500 pessoas** decidiram te processar ao mesmo tempo. rsrs 💸
* **Total da brincadeira:** R$ 1.000.000,00 só de indenização, sem contar as multas da LGPD que podem chegar a 2% do faturamento.

Quem paga a conta no final? Eu garanto que não é o estagiário — embora ele vá pagar sendo demitido roro

No fim, se o tratamento dos dados foi feito com ferramentas de cloud ou não, a conta vai ser a mesma. Por isso, vamos tratar os dados com carinho!!
## 🧪 Conclusão do caso
O NER até sabe quem eu sou, mas o PII não quer me proteger. Essa inconsistência prova que a inteligência artificial, por mais "inteligente" que pareça, ainda precisa de um olhar humano (e brasileiro) para não virar um pesadelo.

`**Spoiler:** É por causa desse "bug cultural" que eu decidi que não dava para confiar apenas na IA nativa. No módulo de comparação, vou mostrar como a futura gatinha engenheira de software (e javeira estilosa) resolveria o que o Azure ignora.` 

---
*Desenvolvido com indignação técnica por [Jaiane/JaiDev-bot].*




