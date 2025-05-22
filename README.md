# 🚀 Guia: Configuração Básica do Git no Windows  

Este guia explica o processo para configurar o Git corretamente no Windows, desde a instalação até a primeira configuração e uso no Git Bash.  

## 1️⃣ Instalar o Git  
1. Acesse o site oficial do Git: [https://git-scm.com/](https://git-scm.com/)  
2. Baixe e instale a versão mais recente para Windows.  
3. Durante a instalação, **selecione Git Bash** como terminal preferido.  

## 2️⃣ Abrir o Terminal Correto  
📌 **Importante:** Para evitar problemas, **sempre use o Git Bash** em vez do Git CMD ou Prompt de Comando do Windows.  
- Para abrir o **Git Bash**, basta procurar `Git Bash` no Menu Iniciar do Windows e clicar.  

## 3️⃣ Configurar Git com Nome e Email  
Depois de abrir o Git Bash, configure seu nome e email para que seus commits sejam identificados corretamente:  
```sh
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@example.com"
```
Verifique se as configurações foram salvas corretamente:  
```sh
git config --global --list
```

## 4️⃣ Criar um Repositório  
Agora, vamos criar um repositório para testar:  
```sh
mkdir meu_projeto
cd meu_projeto
git init
```
Isso inicializa um novo repositório Git dentro da pasta `meu_projeto`.  

## 5️⃣ Adicionar Arquivos e Criar um Commit  
Crie um arquivo de teste e registre as mudanças no Git:  
```sh
echo "Meu primeiro arquivo" > arquivo.txt
git add arquivo.txt
git commit -m "Adicionando primeiro arquivo ao repositório"
```

## 6️⃣ Conectar ao GitHub  
Caso seu repositório já esteja criado no GitHub, conecte-o ao repositório remoto:  
```sh
git remote add origin https://github.com/seuusuario/seurepositorio.git
git push -u origin main
```

## 7️⃣ Trabalhar com Branches  
Se quiser criar uma branch nova para desenvolvimento:  
```sh
git checkout -b feature/nova-funcionalidade
```
Depois de fazer alterações, mescle com a `main`:  
```sh
git checkout main
git merge feature/nova-funcionalidade
git push origin main
```

---

📌 **Dica:** Se precisar resolver conflitos de merge, edite os arquivos manualmente e use:  
```sh
git add .
git commit -m "Resolvendo conflitos de merge"
git push origin main
```

Esse passo a passo cobre tudo para começar no Git no Windows da maneira correta! 😊 
