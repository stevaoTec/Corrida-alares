# Corrida Alares — publicação
1. Configuração Web já preenchida para gta6-88155. Abra esse projeto no Firebase Console.
2. Ative Authentication > Email/senha e crie o usuário administrador. Copie seu UID. Configure o mesmo e-mail técnico em window.AlaresAdminEmail no firebase-config.js (por exemplo, admin@corrida.example). O administrador digita somente a senha na interface.
3. Crie Firestore em modo produção. Publique o conteúdo de firestore.rules na aba Regras.
4. No console Firestore crie a coleção admins e um documento cujo ID seja o UID do administrador (campo enabled=true, booleano). Não conceda acesso de escrita público.
5. Suba index.html, firebase-config.js e vercel.json ao GitHub e importe na Vercel, preset Other, sem build. Use um plano adequado ao uso empresarial.
6. Adicione o domínio Vercel aos domínios autorizados do Firebase Authentication. Abra o site, entre somente com a senha do administrador e salve uma alteração para criar a corrida compartilhada. Para migrar dados antigos, exporte JSON na versão anterior e importe no painel novo.
7. Teste em dois navegadores: registre venda no admin, confira movimento no visitante; recarregue e confira persistência. Teste acesso sem login e senha incorreta.

Sem configuração Firebase não há gravação administrativa. Não coloque senhas ou chaves privadas no repositório. Dados da corrida são públicos; não inclua dados pessoais desnecessários. O modo demo altera a campanha real. Não há contador de visitantes implementado.
