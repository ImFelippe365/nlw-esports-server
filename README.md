# NLW eSports Back-End ![Badge](https://img.shields.io/static/v1?label=prisma&message=5.4.8&color=white&style=flat&logo=PRISMA) ![Badge](https://img.shields.io/static/v1?label=nodejs&message=v16.13.2&color=green&style=flat&logo=NODE) ![Badge](https://img.shields.io/static/v1?label=typescript&message=v4.8.3&color=blue&style=flat&logo=TYPESCRIPT)
 
<br />
<p align="center">
  <img src="https://github.com/ImFelippe365/nlw-esports-mobile/blob/main/src/assets/logo-nlw-esports%402x.png" />
</p>
<br />

Aplicação back-end para surprir as necessidades de dados das demais plataformas desenvolvidas que são citadas mais abaixo. 
Este sistema é capaz de listar os jogos disponíveis, seus respectivos anúncios e cadastrar novos anúncios de um jogo.

Durante o evento do NLW da Rocketseat, essa foi a aplicação a ser desenvolvida durante o evento.
E ao decorrer dos 6 dias, este foi o resultado final da parte do back-end.

Além do atual projeto, foi desenvolvido uma aplicação mobile e para web, na qual requisitam os dados para essa API.

- **[NLW eSports Mobile](https://github.com/ImFelippe365/nlw-esports-mobile)**
- **[NLW eSports Web](https://github.com/ImFelippe365/nlw-esports-web)**

## Tecnologias utilizadas no projeto

- Prisma
- NodeJS
- TypeScript

## Rotas
Importante ressaltar que localmente a url para acesso é ``localhost:3333``, caso o repositório seja hospedado em um servidor é necessário revisar essas informações na hora de usufruir da API.

### Listar jogos

```ts
get('/games/')
```

Saída:
```json
[
	{
		"id": "e5bdc648-c1bf-4cc1-8721-a548d58775b5",
		"title": "League of Legends",
		"bannerUrl": "https://static-cdn.jtvnw.net/ttv-boxart/21779-285x380.jpg",
		"_count": {
			"ads": 0
		}
	},
	{
		"id": "6cf741e6-9893-44a8-931f-414b083de6aa",
		"title": "Minecraft",
		"bannerUrl": "https://static-cdn.jtvnw.net/ttv-boxart/27471_IGDB-285x380.jpg",
		"_count": {
			"ads": 0
		}
 },
]
```

### Listar anúncios de um jogo

```ts
get('/games/id/ads')
```

Saída:
```json
[
 {
		"id": "c8e82ced-6878-4cad-8ea0-466320de00ff",
		"name": "ImFelippe365",
		"weekDays": [
			"0",
			"6"
		],
		"useVoiceChannel": true,
		"yearsPlaying": 2,
		"hoursStart": "13:00",
		"hoursEnd": "18:00"
	}
]
```

## Instalação

Para instalar e usar pelo repositório, clone o repositório e instale as dependências usando o seguinte comando no diretório raiz.

```
npm install
```

ou se preferir:

```
yarn install
```

## Executar

E por fim, para executar o projeto basta inserir o seguinte comando:

```
npm run dev
```

ou se preferir:

```
yarn dev
```
