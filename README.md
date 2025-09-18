# 🏗️ Desafio de Projeto: Infraestrutura como Código com AWS CloudFormation

Este projeto foi desenvolvido como parte de um **desafio prático** para aplicar os conceitos de **Infraestrutura como Código (IaC)** utilizando o serviço **AWS CloudFormation**.  
O objetivo principal foi **automatizar o provisionamento de recursos na nuvem da AWS**, como instâncias EC2, servidores web e regras de segurança, através de **templates declarativos**.

---

## 🎯 Objetivos de Aprendizagem
Ao final deste laboratório, fui capaz de:

- Aplicar conceitos de IaC em um ambiente prático na AWS.  
- Criar e gerenciar **Stacks** no CloudFormation.  
- Estruturar **templates em YAML** para definir recursos de nuvem.  
- Documentar processos técnicos de forma clara e estruturada.  
- Utilizar o **GitHub** para compartilhar a documentação e os templates do projeto.  

---

## 🛠️ Execução e Evidências do Laboratório

A prática foi dividida em múltiplos experimentos, criando **pilhas (Stacks) independentes** para entender o provisionamento de cada componente da infraestrutura.

### 1. Processo de Criação da Pilha no Console
O primeiro passo para cada experimento foi realizar o **upload do template YAML** correspondente através do **console do AWS CloudFormation**, utilizando a opção:  
👉 *"Fazer upload de um arquivo de modelo"*
<img width="1920" height="1080" alt="modelo" src="https://github.com/user-attachments/assets/64827fa7-0a27-43b3-af11-b1562c811d8a" />

---

### 2. Experimento: Stack `lab-ec2`
- **Objetivo:** Criar uma instância EC2 simples, sem configurações adicionais, para validar o processo básico de provisionamento.  
- **Resultado no CloudFormation:** A pilha `lab-ec2` foi criada com sucesso, como pode ser visto na aba **Recursos**.
<img width="1920" height="1080" alt="lab-ec2" src="https://github.com/user-attachments/assets/c55925ee-b597-4f03-b27b-d82a45693e4f" />

- **Resultado no EC2:** A instância correspondente foi provisionada e estava em **estado de execução**.
  
<img width="1920" height="1080" alt="ec2-criada" src="https://github.com/user-attachments/assets/49288130-f6b8-4743-86c2-3c23606c37a1" />

---

### 3. Experimento: Stack `lab-apache`
- **Objetivo:** Provisionar uma instância EC2 e, durante sua inicialização, instalar e configurar um servidor web **Apache** automaticamente via **UserData**.  
- **Resultado no CloudFormation:** A pilha `lab-apache` foi executada com sucesso, conforme o **log de eventos**.
<img width="1920" height="1080" alt="lab-apache" src="https://github.com/user-attachments/assets/fbbe49d9-ec57-4058-ade7-f03206b24d14" />

- **Resultado no EC2:** A instância `Webserver` foi criada, configurada e já possuía um **endereço IP público** para acesso ao site.  
<img width="1920" height="1080" alt="instancia-apache" src="https://github.com/user-attachments/assets/aad621ea-e71d-4191-94de-819c3af77b65" />

---

### 4. Experimento: Stack `lab-grupo-seguranca`
- **Objetivo:** Modularizar a infraestrutura, criando um **Grupo de Segurança (firewall)** em uma pilha separada.  
- **Resultado no CloudFormation:** A pilha `lab-grupo-seguranca` foi criada com sucesso, juntamente com as outras pilhas do laboratório.
<img width="1920" height="1080" alt="lab-grupo-seguranca" src="https://github.com/user-attachments/assets/09809dca-0216-4723-b857-64c1415d4195" />

- **Resultado no EC2 (Grupo de Segurança):** O Grupo de Segurança foi criado com a descrição e as **regras de entrada para HTTP (porta 80)** definidas no template.
<img width="1920" height="1080" alt="grupo-seguranca" src="https://github.com/user-attachments/assets/159d365d-007f-430a-95e6-5252f62d66ae" />

- **Resultado no EC2 (Instâncias):** No painel do EC2, é possível ver todas as instâncias criadas pelos diferentes laboratórios, que utilizariam os grupos de segurança para controlar seu tráfego.  
<img width="1920" height="1080" alt="instancia-grupo" src="https://github.com/user-attachments/assets/4c91333d-b7a9-4dc6-bdf9-46d73741591e" />

---

## 💡 Insights e Conclusão

- Este desafio prático foi fundamental para solidificar o entendimento sobre o poder da **Infraestrutura como Código**.  

- A principal vantagem observada é a capacidade de **criar, replicar e destruir ambientes inteiros** de forma rápida, consistente e com **controle de versão**.  

- O **CloudFormation** elimina a necessidade de configuração manual, reduzindo drasticamente o risco de erros humanos e garantindo que a infraestrutura implantada seja exatamente a que foi declarada no código.  

- A experimentação com **pilhas modulares** (separando o grupo de segurança da instância, por exemplo) também abriu a visão para a criação de **templates reutilizáveis** em arquiteturas mais complexas no futuro.  
---

## ✨ Autora

**Ingrid Moitinho**

* LinkedIn: [LinkedIn](https://www.linkedin.com/in/ingridmoitinho/)
* GitHub: [GitHub](https://github.com/ingridmoitinho)
