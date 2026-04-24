# 👋 Bem-vindo ao meu GitHub!

Olá! Sou **Douglas Kauã Zinh**, estudante de **Engenharia da Computação** apaixonado por desenvolvimento de software e resolução de problemas através da programação.

---

## 🎓 Sobre Mim

- 🎯 Estudante de **Engenharia da Computação**
- 💻 Desenvolvedor em formação com foco em **linguagem C** e desenvolvimento de sistemas
- 🚀 Aprendendo e evoluindo constantemente
- 🎮 Interessado em desenvolvimento de jogos e aplicações interativas

---

## 🛠️ Linguagens & Tecnologias

```
C           ████████░░ 80%
Git         ██████░░░░ 60%
Terminal    ██████░░░░ 60%
Sistemas    ████████░░ 80%
```

- **Linguagens**: C
- **Ferramentas**: Git, GitHub, Terminal/Shell
- **Foco**: Desenvolvimento de sistemas, algoritmos, estruturas de dados

---

## 🎮 Meus Projetos em Destaque

### 🕹️ [Projeto C - Jogos](https://github.com/douglaskauazinh-collab/projeto-c-jogos)

Um programa desenvolvido em **linguagem C** que reúne vários **mini jogos** em um único sistema interativo via terminal.

O usuário pode escolher entre diferentes opções através de um menu, tornando a experiência simples e dinâmica.

#### 🕹️ Funcionalidades

- **❓ Pergunta e Resposta** - Um mini jogo de perguntas onde o usuário testa seus conhecimentos.
- **🐍 Cobra na Caixa** - Um jogo de sorte onde o jogador deve escolher caixas sem encontrar a cobra.
- **⚔️ Gousmas War** - Um jogo para dois jogadores baseado em estratégia, onde cada jogador controla suas "gousmas" e tenta derrotar o adversário.
- **🚪 Sair** - Encerra o programa.

#### 💡 Tecnologias Utilizadas

- Linguagem C
- Biblioteca padrão (stdio.h, stdlib.h, time.h)
- Sistema via Terminal

---

## 💾 Código Principal

Aqui está o código completo que faz todo o projeto funcionar:

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
	
	srand(time(NULL));
	
	
	 int opcao;
	 
	 do {
	 	printf("\n=== menu ===\n");
	 	printf("1 - pergunta e resposta\n");
	 	printf("2 - cobra na caixa\n");
	 	printf("3 - gousmas war\n");
	 	printf("4 - sair\n");
	 	printf("escolha uma opcao: ");
	 	scanf("%d", &opcao);
	 	
	 	switch(opcao) {
	 		case 1:
	 			printf("\n=== PERGUNTAS E RESPOSTAS ===\n");
	 			
	 			int resposta;
	 			int acertos = 0;
	 			
	 			// PERGUNTA 1
	 			printf("1) qual dessas pecas e responsavel por processar as informacoes do computador?\n");
	 			printf("----------------------------------\n");
	 			printf("1) HD\n2) Monitor\n3) processador\n4) teclado\n");
	 			scanf("%d", &resposta);
    
	 			if (resposta == 3) {
	 				printf("correto!\n");
	 				acertos++;
				 } else {
				 	printf("incorreto! resposta correta: processador\n");
				 }
				 
				 // PERGUNTA 2
				 printf("2) qual dessas pecas e usada para armazenar arquivos?\n");
				 printf("----------------------------------\n");
				 printf("1) memoria ram\n2) HD\n3) mouse\n4) fonte\n");
				 scanf("%d", &resposta);
				 
				 if (resposta == 2) {
				 	printf("correto!\n");
				 	acertos++;
				 } else {
				 	printf("incorreto! resposta correta: HD\n");
				 }
				 
				 // PERGUNTA 3
				 printf("3) qual desses dispositivos voce usa para mover o cursor na tela?\n");
				 printf("----------------------------------\n");
				 printf("1) teclado\n2) monitor\n3) mouse\n4) gabinete\n");
				 scanf("%d", &resposta);
				 
				 if (resposta == 3) {
				 	printf("correto!\n");
				 	acertos++;
				 } else {
				 	printf("incorreto! resposta correta: mouse\n");
				 }
				 
				 // PERGUNTA 4
				 printf("4) qual dessas pecas mostra as imagens do computador?\n");
				 printf("----------------------------------\n");
				 printf("1) placa mae\n2) monitor\n3) HD\n4) processador\n");
				 scanf("%d", &resposta);
				 
				 if(resposta == 2) {
				 	printf("correto!\n");
				 	acertos++;
				 } else {
				 	printf("incorreto! resposta correta: monitor\n");
				 }
				 
				 // PERGUNTA 5
				 printf("5) qual dessas pecas fornece energia para o computador funcionar?\n");
				 printf("----------------------------------\n");
				 printf("1) fonte\n2) mouse\n3) teclado\n4) memoria ram\n");
				 scanf("%d", &resposta);
				 
				 if (resposta == 1) {
				 	printf("correto!\n");
				 	acertos++;
				 } else {
				 	printf("incorreto! resposta correta: fonte\n");
				 }
				 
				 // RESULTADO FINAL
				 printf("\nvoce acertou %d de 5 perguntas!\n", acertos);
				 
				 break;
		 
 	    
	 		case 2: {
	 			int jogar;
	 			
	 			do {
	 				int caixa_botao, caixa_cobra;
	 				int caixas_abertas[5] = {0,0,0,0,0};
	 				int p1, p2, turno, fim, escolha;
	 				int i;
	 				
	 				char nomes[7][20] = {
	 					"ana","kamila","kaua",
	 					"pedro","eduardo","gabriel","sophia"
	 					
					 };
					 
					 printf("\n=== COBRA NA CAIXA ===\n");
					 
					 // jogador 1
					 do {
					 	printf("jogador 1 escolha (1-7):\n");
					 	for (i = 0; i < 7; i++) {
					 		printf("%d - %s\n", i+1, nomes[i]);
						 }
						 scanf("%d", &p1);
						 
						 if (p1 < 1 || p1 > 7)
						 	printf("numero invalido!\n");
						 
					 } while (p1 < 1 || p1 > 7);
					 
					 // jogador 2 
					 do {
					 	printf("jogador 2 escolha outro (1-7): ");
					 	scanf("%d", &p2);
					 	
					 	if (p2 < 1 || p2 > 7)
					 		printf("numero invalido!\n");
					 	else if (p2 == p1)
					 		printf("nome ja escolhido!\n");
					 	
					 } while (p2 < 1 || p2 > 7 || p2 == p1);
					 
					 // sorteios
					 turno = rand() % 2 + 1;
					 
					 caixa_botao = rand() % 5;
					 do {
					 	caixa_cobra = rand() % 5;
					 } while (caixa_cobra == caixa_botao);
					 
					 fim = 0;
					 
					 printf("\n%s comeca!\n", (turno == 1) ? nomes[p1-1] : nomes[p2-1]);
					 
					 while (!fim) {
					 	
					 	printf("\nCaixas disponiveis:\n");
					 	for (i = 0; i < 5; i++) {
					 		if  (caixas_abertas[i] == 0)
					 			printf("caixa %d\n", i+1);
						 }
						 
						 printf("%s escolha uma caixa: ", (turno == 1) ? nomes[p1-1] : nomes[p2-1]);
						 scanf("%d", &escolha);
						 
						 escolha--;
						 
						 if (escolha < 0 || escolha > 4 || caixas_abertas [escolha] ==1) {
						 	printf("escolha invalida!\n");
						 	continue;
						 }
						 
						 caixas_abertas[escolha] = 1; 
						 
						 if (escolha == caixa_botao) {
						 	printf(" BOTAO! %s venceu!\n",(turno == 1) ? nomes [p1-1] : nomes [p2-1]);
						 	fim = 1;
						 }
						 else if (escolha == caixa_cobra) {
						 	printf(" COBRA! %s perdeu!\n", (turno == 1) ? nomes [p1-1] : nomes [p2-1]);
						 	fim = 1;
						 }
						 else {
						 	printf("caixa vazia...\n");
						 	turno = (turno == 1) ? 2 : 1;
						 }
					 }
					 
					 printf("\n1 - jogar novamente\n2 - voltar ao menu\n");
					 scanf("%d", &jogar);
					 
				 } while (jogar == 1); 
				 
				 break;
			 }
					 	
	 		case 3:
			 	printf("voce escolheu gousmas war\n");
			 	break;
			 case 4:
			 	printf("saindo...\n");
			 	break;
			 default:
			 	printf("opcao invalida!\n");
			 	
		 }
		 
	 } while(opcao != 4);
	 
	 return 0;
	 
  }
```

---

## 📊 GitHub Stats

![Linguagens mais usadas](https://github-readme-stats.vercel.app/api/top-langs/?username=douglaskauazinh-collab&layout=compact&theme=dark)

---

## 🌱 Atualmente Aprendendo

- 📚 Estruturas de dados avançadas
- 🎮 Desenvolvimento de jogos
- 🔗 Sistemas e algoritmos
- 🚀 Boas práticas de programação

---

## 💬 Vamos nos Conectar?

Sinta-se à vontade para explorar meus repositórios e contribuir com sugestões e feedback!

- 📌 GitHub: [@douglaskauazinh-collab](https://github.com/douglaskauazinh-collab)
- 📌 Perfil: [@douglaskauazinh-collabFirst](https://github.com/douglaskauazinh-collabFirst)

---

## ⚡ Fun Facts

- 🎯 Apaixonado por desafios de programação
- 💡 Sempre buscando aprender algo novo
- 🎮 Gosto de criar experiências interativas

---

**⭐ Se você gostou de algum projeto, considere deixar uma estrela! ⭐**

```
╔═══════════════════════════════════════╗
║  Obrigado pela visita! Happy Coding!  ║
╚═══════════════════════════════════════╝
```
