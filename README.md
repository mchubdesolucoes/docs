# RelaxPay Documentation

Documentação oficial da API RelaxPay, um gateway de pagamento moderno e intuitivo para integração de PIX.

## Melhorias Implementadas

- **Páginas Interativas**: Todas as páginas foram redesenhadas para incluir elementos interativos do Mintlify
- **Exemplos Multi-linguagem**: Exemplos de código em JavaScript, PHP, Python e C#
- **Cards com Links**: Cards clicáveis que redirecionam para as páginas correspondentes
- **Testadores Embutidos**: Ferramentas para testar a API diretamente na documentação
- **Fluxos Visuais**: Imagens e diagramas que explicam os processos de integração
- **Página de Erros Centralizada**: Uma página dedicada com todos os códigos de erro e soluções
- **Design Consistente**: Padronização visual em todas as páginas
- **Componentes Enriquecidos**: Uso de Tabs, Cards, Steps e outros componentes para melhor organização
- **Playground da API**: Interface interativa para testar os endpoints da API diretamente na documentação
- **Especificação OpenAPI**: Documentação completa da API no formato OpenAPI (Swagger)

## Desenvolvimento

Para executar a documentação localmente:

1. Instale o [Mintlify CLI](https://www.npmjs.com/package/mintlify):
```bash
npm i -g mintlify
```

2. Execute o servidor de desenvolvimento:
```bash
mintlify dev
```

A documentação estará disponível em `http://localhost:3000`.

## Estrutura do Projeto

- `/introduction.mdx` - Página de boas-vindas e visão geral
- `/gateway/` - Documentação principal da API
  - `/gateway/authentication.mdx` - Autenticação na API
  - `/gateway/environments.mdx` - Ambientes de desenvolvimento e produção
  - `/gateway/pix-cash-in.mdx` - Recebimento de pagamentos PIX
  - `/gateway/pix-cash-out.mdx` - Envio de pagamentos PIX
  - `/gateway/webhooks.mdx` - Sistema de notificações
  - `/gateway/errors.mdx` - Códigos de erro e soluções
- `/api/` - Documentação da API no formato OpenAPI
  - `/api/openapi.yaml` - Especificação OpenAPI da API RelaxPay
- `/api-reference.mdx` - Página com playground interativo da API
- `/images/` - Imagens utilizadas na documentação
- `/docs.json` - Configuração do Mintlify

## Playground da API

A documentação inclui um playground interativo da API que permite:

- Testar os endpoints da API diretamente na documentação
- Visualizar a estrutura de requisições e respostas
- Entender os parâmetros necessários para cada operação
- Experimentar a API antes de implementar o código

Para utilizar o playground:

1. Acesse a página "Referência da API" na documentação
2. Insira suas credenciais de sandbox (Client ID e Client Secret)
3. Selecione o endpoint desejado
4. Preencha os parâmetros necessários
5. Clique em "Enviar" para testar a requisição

## Imagens

As imagens na pasta `/images/` são placeholders e devem ser substituídas por imagens reais antes da publicação. Sugerimos a criação das seguintes imagens:

- `auth-dashboard.png` - Tela do dashboard de obtenção de credenciais
- `webhooks-flow.png` - Diagrama do fluxo de webhooks
- `pix-cash-in-flow.png` - Diagrama do fluxo de PIX Cash-in
- `pix-cash-out-flow.png` - Diagrama do fluxo de PIX Cash-out
- `auth-flow.png` - Diagrama do fluxo de autenticação
- `ip-management.png` - Tela de gerenciamento de IPs autorizados

## Contribuição

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## Suporte

Para suporte, entre em contato:
📧 **suporte@relaxpay.app**
