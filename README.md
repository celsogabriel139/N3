# N3
**A aplicação Android e o seu Ciclo de Vida**

O ciclo de vida de uma aplicação Android é fundamental para entender como a aplicação interage com o ambiente e como o sistema operacional gerencia seus recursos. Cada componente da aplicação, como 'Activities' ou os 'Services' seguem esse conceito da ordem desse ciclo pré-definido pela linguagem do próprio Kotlin (Android).

Acontece que a 'Activity' não é algo totalmente estático durante seu funcionamento, devido ao fluxo de dados, a mesma é submetida a funções (ou métodos) que influenciam em seu funcionamento em determinada etapa. A importãncia desse processo de ciclo de 'vida' da Activity se deve ao fato de que isso auxilia precisamente no quesito de **recurso de dados.** Para exemplificar, segue cada uma das etapas desse ciclo de vida e suas respectivas explicações:

1. onCreate(): Usado quando estamos criando a Activity. Aqui é onde você configura a interface do usuário e inicializa variáveis que deverão receber os valores.
2. onStart(): Usamos para tornar a Activity visível, após os a interface e ses valores tiverem sido definidos (Inicializar)
3. onResume(): Usamos quando a Activity está visível e pronta para interação com o usuário.
4. onPause(): Chamamos este quando outra Activity entra em primeiro plano, mas a Activity atual ainda é visível (por exemplo, quando uma janela de diálogo é exibida). Aqui você pode salvar dados que devem persistir. Praticamente uma espécie de "pausa" na atividade da Activity.
5. onStop(): Chamado quando a Activity não está mais visível.
6. onDestroy(): Chamado quando queremos que a Activity seja "destruída", ou seja, liberar dados que não vão ser mais úteis, que ficariam ocupando um espaço na memória de maneira desnecessária.

Cada um desses pontos é importante porque permite que você gerencie como sua aplicação se comporta, sem excessão. O maior proveito que pode-se ser tirado de um ciclo de vida de uma Activity recai sobre o uso devido de cada um dos seus respectivos métodos.
