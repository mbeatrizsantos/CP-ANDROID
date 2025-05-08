**ANDROID CRYPTOR MONITOR**

Aplicativo Android desenvolvido em Kotlin para monitorar a cotação do Bitcoin (BTC) em reais (BRL), utilizando uma API pública. O projeto tem como objetivo demonstrar boas práticas no desenvolvimento mobile, especialmente no consumo de APIs REST e na aplicação da arquitetura MVVM com componentes modernos do Android.

**Objetivo do Projeto**

- Demonstrar o consumo de uma API externa utilizando Retrofit.
- Aplicar a arquitetura MVVM para separação de responsabilidades.
- Trabalhar com chamadas assíncronas usando Coroutines.
- Atualizar dinamicamente a interface com LiveData e ViewModel.
- Exibir informações de forma simples, objetiva e funcional.

**Funcionalidades**

- Consulta sob demanda do valor do Bitcoin em reais.
- Exibição do valor com formatação monetária.
- Indicação da data e hora da última atualização.
- Interface enxuta com foco na usabilidade.

**Tecnologias e Conceitos Utilizados**

**Kotlin**
Linguagem oficial recomendada para o desenvolvimento Android, moderna, segura e expressiva.

**MVVM (Model - View - ViewModel)**
Arquitetura que separa a lógica de apresentação (ViewModel) da camada de visualização (View), promovendo organização, testabilidade e manutenção do código.

**Retrofit**
Biblioteca de cliente HTTP utilizada para fazer chamadas à API pública de cotações (AwesomeAPI) de forma segura, eficiente e baseada em interfaces.

**Coroutines**
Recurso da linguagem Kotlin que permite realizar operações assíncronas (como chamadas de rede) de forma simples e sem bloqueio da interface do usuário.

**LiveData**
Classe observável que permite que a interface responda automaticamente a alterações nos dados, garantindo uma UI reativa e atualizada.

**ViewModel**
Responsável por manter e gerenciar os dados da interface de forma desacoplada do ciclo de vida da Activity, evitando perda de dados em mudanças de configuração.

**View Binding**
Mecanismo que facilita o acesso aos elementos de layout XML de forma segura e com verificação em tempo de compilação, substituindo o uso de findViewById.

**Gradle Kotlin DSL**
Utilização de arquivos build.gradle.kts para configurar o projeto com uma sintaxe mais segura e integrada com o Kotlin.


**Funcionamento do App**

- O aplicativo exibe inicialmente o valor "R$ 0,00" como padrão.
- Ao clicar no botão "ATUALIZAR":
- O ViewModel inicia o processo de obtenção dos dados.
- A Repository faz a chamada à API através do Retrofit.
- Os dados retornam no formato JSON e são convertidos para o modelo CryptoResponse.
- O valor e a data são atualizados no LiveData.
- A Activity observa o LiveData e atualiza automaticamente a interface com as novas informações.


**- Tela com valor inicial:**

  ![image](https://github.com/user-attachments/assets/71b3d84d-7012-4d0c-be61-94ad50953741)


 **- Tela com valor depois de clicar no botão "atualizar":**
    
  ![image](https://github.com/user-attachments/assets/d33605f9-8aa7-4ab4-880a-7b144155ae45)


