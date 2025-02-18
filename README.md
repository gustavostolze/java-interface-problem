# Problema exemplo

 Uma locadora brasileira de carros cobra um valor por hora para locações de até 12 horas. Porém, se a duração da locação ultrapassar 12 horas, a locação será cobrada com base em um valor diário. Além do valor da locação, é acrescido no preço o valor do imposto conforme regras do país que, no caso do Brasil, é 20%para valores até 100.00, ou 15% para valores acima de 100.00. Fazer um programa que lê os dados da locação (modelo do carro, instante inicial e final da locação), bem como o valor por hora e o valor diário de locação. O programa deve então gerar a nota de pagamento (contendo valor da locação, valor do imposto e valor total do pagamento) e informar os dados na tela. Veja os exemplos.

![image](https://github.com/user-attachments/assets/e2501475-fafc-45d0-8b6c-dda289772de1)

Problemática da seguinte implementação sem utilização de interfaces: 

![image](https://github.com/user-attachments/assets/ef965091-4fee-40fc-9d03-540682b48875)

 Se for necessário realizar algum tipo de manuntenção nessa camada do projeto, o RentalService estar associado ao BrazilTaxService poderia deixar a possível manuntenção muito complexa. Isso pode ser caso de alto acoplamento. Exemplo: \
 \
 Caso a aplicação começasse a alugar veículos em outros paises, exigiria uma manuntenção onde seria necessário alterar a quem o RentalService está associado, e muita lógica de verificação dentro dele caso fosse possível existir taxas do Brasil, e de um outro país dependendo de alguma verificação.
 
![image](https://github.com/user-attachments/assets/92f23f09-b10f-4530-be4b-125d5c00c196)

Essa implementação de interface, que é uma definição genérica, garante um contrato onde TaxService precisa ter uma operação de imposto, permitindo maior flexibilidade e desacoplamento desse sistema.
