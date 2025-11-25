📌 Padrão de Projeto: Prototype (GoF)
🎯 Objetivo

O padrão Prototype permite criar novos objetos copiando instâncias existentes, evitando construtores caros ou complexos.
Ele é útil quando:

o processo de criação é custoso;

existem diversas combinações de configurações;

você quer evitar o acoplamento com classes concretas ao criar objetos.

1️⃣ Explicação do Problema (Sem Prototype)

Imagine um sistema que cria figuras geométricas (Círculo, Retângulo, etc).
Sem Prototype, para criar novos objetos, você precisa:

Invocar construtores diretamente,

Repetir configuração,

Lidar com dependências e lógica complicada de criação,

Ter várias condicionais if/switch para instanciar classes concretas

3️⃣ Comparação direta: Sem vs Com Prototype
Critério	Sem Prototype	Com Prototype
Criação de objetos semelhantes	Repetitiva e manual	Automática por clonagem
Acoplamento	Alto (usa new)	Baixo (usa clone())
Configuração repetida	Sim	Não
Facilidade para objetos complexos	Difícil	Simples
Performance	Pode ser custosa	Alto desempenho ao copiar objetos
Extensibilidade	Baixa	Alta

4️⃣ Quando usar Prototype?

Use quando:

✔️ Bom cenário

Objetos possuem muitas configurações.

Criação envolve operações caras (consulta a BD, validações, cálculos).

Precisa criar objetos em run-time sem saber a classe concreta.

Precisa criar múltiplas instâncias quase idênticas.

❌ Não usar quando

Objetos são simples.

Não há lógica de criação complexa.

Clonagem profunda é difícil ou insegura (objetos não copiáveis).

5️⃣ Pontos Fortes e Fracos
👍 Pontos fortes

Reduz repetição de código.

Criação rápida de objetos.

Facilita extensão e reutilização.

Desacopla da classe concreta.

Bom para objetos complexos.

👎 Pontos fracos

Clonagem profunda pode ser trabalhosa.

Pode ser confuso quando há muitos objetos interdependentes.

Requer cuidado com objetos mutáveis.

6️⃣ Conclusão 

O padrão Prototype é útil quando:

o sistema precisa criar muitas instâncias semelhantes,

a lógica de criação é pesada ou complexa,

quer reduzir o acoplamento entre classes e melhorar a flexibilidade.

Em projetos onde velocidade e simplicidade são essenciais, Prototype oferece uma forma clara e eficiente de duplicar objetos. Porém, deve ser aplicado com cuidado quando a clonagem envolve estruturas de dados complexas.

🆚 Comparação
❌ Sem Prototype

Criação repetitiva

Baixa reutilização

Alto acoplamento

✔️ Com Prototype

Reutilização máxima

Baixo acoplamento

Criação rápida de objetos complexos
