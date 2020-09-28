---
title: Publicar um pacote
intro: 'Você pode publicar um pacote no {{ site.data.variables.product.prodname_registry }} para disponibilizar o pacote para que outros façam download e reutilizem.'
product: '{{ site.data.reusables.gated-features.packages }}'
redirect_from:
  - /github/managing-packages-with-github-packages/publishing-a-package
permissions: Qualquer pessoa com permissões de gravação para um repositório pode publicar um pacote nesse repositório.
versions:
  free-pro-team: '*'
  enterprise-server: '>=2.22'
---

{{ site.data.reusables.package_registry.packages-ghes-release-stage }}

### Sobre os pacotes publicados

Você pode ajudar as pessoas a entender e usar seu pacote fornecendo uma descrição e outros detalhes como, por exemplo, a instalação e instruções de uso na página do pacote. GitHub provides metadata for each version, such as the publication date, download activity, and recent versions. Para uma página de pacote de exemplo, veja [@Codertocat/hello-world-npm](https://github.com/Codertocat/hello-world-npm/packages/10696?version=1.0.1).

{{ site.data.reusables.package_registry.public-or-private-packages }} Um repositório pode conter mais de um pacote. Para evitar confusão, certifique-se de que o LEIAME e a descrição fornecem informações claras sobre cada pacote.

{{ site.data.reusables.package_registry.package-immutability }}

{% if currentVersion == "free-pro-team@latest" %}
Se uma nova versão de um pacote corrigir uma vulnerabilidade de segurança, você deverá publicar uma consultoria de segurança no seu repositório. {{ site.data.variables.product.prodname_dotcom }} revisa cada consultoria de segurança publicada e pode usá-la para enviar alertas de {{ site.data.variables.product.prodname_dependabot_short }} para repositórios afetados. Para obter mais informações, consulte "[Sobre as consultorias de segurança do GitHub](/github/managing-security-vulnerabilities/about-github-security-advisories)."
{% endif %}

### Publicar um pacote

You can publish a package to {{ site.data.variables.product.prodname_registry }} using any supported package client by following the same general guidelines.

1. Crie ou use um token de acesso existente com os escopos apropriados para a tarefa que você deseja realizar. Para obter mais informações, consulte "[Sobre {{ site.data.variables.product.prodname_registry }}](/packages/publishing-and-managing-packages/about-github-packages#authenticating-to-github-packages)."
2. Efetue a autenticação em {{ site.data.variables.product.prodname_registry }} usando seu token de acesso e as instruções para seu cliente do pacote.
3. Publique o pacote usando as instruções do seu cliente de pacote.

Para obter instruções específicas para o seu cliente de pacotes, consulte "[Usar o {{ site.data.variables.product.prodname_registry }} com o ecossistema do seu projeto](/packages/using-github-packages-with-your-projects-ecosystem)".

Após publicar um pacote, você poderá visualizá-lo no {{ site.data.variables.product.prodname_dotcom }}. Para obter mais informações, consulte “[Visualizar pacotes](/packages/publishing-and-managing-packages/viewing-packages).”