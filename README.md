🔷 Padrão de Projeto: Prototype 
🛠️ Objetivo

O padrão Prototype permite criar novos objetos a partir da cópia de instâncias existentes, evitando construtores caros, repetitivos ou complexos. Ele é especialmente útil quando:

o processo de criação é custoso;

existem muitas combinações de configurações;

você deseja reduzir o acoplamento e evitar instanciar classes concretas diretamente.

1️⃣ Problema (Sem usar Prototype)

Imagine um sistema que cria figuras geométricas (Círculo, Retângulo, etc.).
Sem o padrão Prototype, para gerar novas instâncias você precisa:

invocar construtores diretamente (new);

repetir configurações comuns;

lidar com dependências e lógica de criação complexa;

usar condicionais (if/switch) para decidir qual classe concreta instanciar.

Esse processo cria acoplamento alto, código repetitivo e difícil manutenção.

2️⃣ Comparação: Sem Prototype vs Com Prototype
Critério	Sem Prototype	Com Prototype
Criação de objetos semelhantes	Repetitiva e manual	Automática por clonagem
Acoplamento	Alto	Baixo
Configuração repetida	Sim	Não
Objetos complexos	Difícil	Eficiente
Desempenho	Simples	Rápido ao copiar
Extensibilidade	Baixa	Alta

3️⃣ Quando usar Prototype?
🧩 Cenários ideais

Use Prototype quando:

os objetos têm muitas configurações;

a criação envolve operações custosas (BD, cálculos, validações);

é necessário criar objetos sem conhecer a classe concreta;

várias instâncias semelhantes precisam ser geradas rapidamente.

⚠️ Quando evitar

Não use Prototype quando:

os objetos são simples;

não há lógica complexa de criação;

a clonagem profunda é difícil ou insegura.

4️⃣ Pontos fortes e fracos
🌟 Vantagens

Reduz código duplicado;

Criação mais rápida para objetos complexos;

Facilita extensão e reaproveitamento;

Desacopla da classe concreta;

bom desempenho em clonagens.

🔻 Desvantagens

Clonagem profunda pode ser trabalhosa;

Pode gerar confusão em sistemas com muitos objetos dependentes;

Exige cuidado com objetos mutáveis.

5️⃣ Conclusão

O padrão Prototype é valioso quando:

há necessidade de criar muitas instâncias semelhantes;

a criação é pesada ou envolve lógica complexa;

deseja-se reduzir acoplamento e aumentar flexibilidade.

Ele oferece uma forma eficiente de duplicar objetos sem reconstruí-los.
Porém, deve ser aplicado com atenção quando a clonagem envolve estruturas complexas ou sensíveis.

🔀 Resumo rápido

Sem Prototype

Código repetitivo

Baixa reutilização

Alto acoplamento

Criação manual e lenta


Com Prototype

Maior reutilização

Baixo acoplamento

Criação rápida de objetos complexos

Menos repetição, mais flexibilidade
