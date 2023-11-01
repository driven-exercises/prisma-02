# prisma-02: Fazendo um upgrade para o Prisma

- Vimos que sendo um ORM, o Prisma poderá nos ajudar a manipular as informações entre o banco de dados e a aplicação.
- Além disso, uma das vantagens do Prisma é que ele é relativamente fácil de ser integrado a projetos legados.
- Para isso, basta seguir os passos iniciais de instalação e a configuração do Prisma.
- ➡️ Refatore o código abaixo e substitua o pg pelo prisma.
- A query deverá ficar assim no `index.ts`:
    
```tsx
// o objeto prisma deve vir do database.ts

(async () => {
    const posts = await prisma.posts.findMany();
    console.log("Posts encontrados no banco:", posts);
})();
```