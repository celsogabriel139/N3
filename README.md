# N3 - A aplicação Android e o Ciclo de Vida da Activity

O ciclo de vida de uma Activity de uma aplicação Android é fundamental para entender como a aplicação interage com o ambiente e como o sistema operacional gerencia seus recursos. Cada componente da aplicação, como 'Activities' ou os 'Services' seguem esse conceito da ordem desse ciclo pré-definido pela linguagem do próprio Kotlin (Android).

Acontece que a 'Activity' não é algo totalmente estático durante seu funcionamento, devido ao fluxo de dados, a mesma é submetida a funções (ou métodos) que influenciam em seu funcionamento em determinada etapa. A importãncia desse processo de ciclo de 'vida' da Activity se deve ao fato de que isso auxilia precisamente no quesito de **recurso de dados.** Para exemplificar, segue cada uma das etapas desse ciclo de vida e suas respectivas explicações:

1. **onCreate()**: Usado quando estamos criando a Activity. Aqui é onde você configura a interface do usuário e inicializa variáveis que deverão receber os valores.
2. **onStart()**: Usamos para tornar a Activity visível, após os a interface e ses valores tiverem sido definidos (Inicializar)
3. **onResume()**: Usamos quando a Activity está visível e pronta para interação com o usuário.
4. **onPause()**: Chamamos este quando outra Activity entra em primeiro plano, mas a Activity atual ainda é visível (por exemplo, quando uma janela de diálogo é exibida). Aqui você pode salvar dados que devem persistir. Praticamente uma espécie de "pausa" na atividade da Activity.
5. **onStop()**: Chamado quando a Activity não está mais visível.
6. **onDestroy()**: Chamado quando queremos que a Activity seja "destruída", ou seja, liberar dados que não vão ser mais úteis, que ficariam ocupando um espaço na memória de maneira desnecessária.

Cada um desses pontos são importantes pois permitem que você gerencie como sua aplicação se comporta, sem excessão. O maior proveito que pode-se ser tirado de um ciclo de vida de uma Activity recai sobre o uso devido de cada um dos seus respectivos métodos. Entre os beneficios pode ser citado a opção de salvar e restaurar o estado da Activity, garantindo que os dados não sejam perdidos durante mudanças de configuração ou interações com o usuário e que a aplicação responda de forma dinâmica às interações do usuário, como por exemplo, igual a "pausar um vídeo" quando a Activity própria é pausada. A pessoa estar mais imersa e no controle do funcionamento da lógica de seu código.

O formato de declaração de cada método se resume em:

**1. onCreate():**

override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_main)
}

**2. onStart():**

override fun onStart() {
    super.onStart()
}

**3. onResume():**

override fun onResume() {
    super.onResume()
}

**4. onPause():**

override fun onPause() {
    super.onPause()
}

**5. onStop():**

override fun onStop() {
    super.onStop()
}

**6. onDestroy():**

override fun onDestroy() {
    super.onDestroy()
}

--

Vale ressaltar que os métodos do ciclo de vida mencionados (onCreate(), onStart(), onResume(), onPause(), onStop() e onDestroy()) não são exclusivos do Kotlin; eles fazem parte da estrutura de desenvolvimento Android e estão presentes em outras linguagens suportadas para Android, como Java.

**Neste mesmo repositório, também está incluso uma imagem que exemplifica todos a ordem de preocesso desses métodos, assim como um código que se utiliza dos mesmos.**


