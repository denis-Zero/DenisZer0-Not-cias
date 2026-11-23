# Firebase do blog GTA6

Arquivos:
- firestore.rules: regras de segurança (leitura pública, escrita só do admin)
- firestore.indexes.json: índices (vazio; o blog não precisa de índice composto)
- firebase.json: liga as regras e os índices ao projeto
- .firebaserc: ID do seu projeto

## Antes de publicar
1. Em firestore.rules, troque `seu-email@gmail.com` pelo seu e-mail de admin.
2. Em .firebaserc, troque `SEU-PROJETO` pelo ID do projeto (Firebase > Configurações do projeto).

## Opção A: pelo site (mais simples)
1. Firebase > Firestore Database > Regras.
2. Cole o conteúdo de firestore.rules e clique em Publicar.

## Opção B: pelo terminal
npm install -g firebase-tools
firebase login
firebase deploy --only firestore

## Também no console do Firebase
- Authentication > Método de login: ativar E-mail/senha e Google.
- Authentication > Configurações > Domínios autorizados: adicionar seuusuario.github.io
- Firestore Database: criar o banco (modo produção).
- A coleção `posts` é criada sozinha na primeira postagem.

## Anúncios e links
As regras agora incluem a coleção `extras` (anúncios e links do painel Adm).
Publique de novo o firestore.rules para o painel poder salvar anúncios e links.
