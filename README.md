<p align="center" width="100%">
<img src="logo/logo.svg" width="500" />
</p>

# RelaxPay Documentation

Documentação oficial da API RelaxPay, um gateway de pagamento moderno e intuitivo para integração de PIX.

## 🚀 Recursos Implementados

| Recurso | Descrição |
|---------|-----------|
| **Múltiplas Versões da API** | Suporte para API v1 (headers) e v2 (Bearer token) |
| **Páginas Interativas** | Todas as páginas foram redesenhadas para incluir elementos interativos do Mintlify |
| **Exemplos Multi-linguagem** | Exemplos de código em JavaScript, PHP, Python e C# |
| **Cards com Links** | Cards clicáveis que redirecionam para as páginas correspondentes |
| **Testadores Embutidos** | Ferramentas para testar a API diretamente na documentação |
| **Fluxos Visuais** | Imagens e diagramas que explicam os processos de integração |
| **Tratamento de Erros** | Página dedicada com todos os códigos de erro e soluções |
| **Design Consistente** | Padronização visual em todas as páginas |
| **Componentes Avançados** | Uso de Tabs, Cards, Steps e outros componentes para melhor organização |
| **Playground da API** | Interface interativa para testar os endpoints da API diretamente na documentação |
| **Especificação OpenAPI** | Documentação completa da API no formato OpenAPI (Swagger) |

## 💻 Desenvolvimento

Para executar a documentação localmente:

```bash
# Instale o Mintlify CLI
npm i -g mintlify

# Execute o servidor de desenvolvimento
mintlify dev
```

A documentação estará disponível em `http://localhost:3000`.

## 📂 Estrutura do Projeto

```
relaxpaydocs/
├── docs.json                # Configuração do Mintlify
├── favicon.svg             # Favicon do site
├── images/                  # Imagens utilizadas na documentação
│   ├── auth-dashboard.png
│   ├── auth-flow.png
│   ├── pix-cash-in-flow.png
│   └── ...
├── introduction.mdx         # Página de boas-vindas e visão geral
├── logo/                    # Logos do projeto
│   └── logo.svg
├── openapi.yaml            # Especificação OpenAPI
├── v1/                      # Documentação da API v1 (autenticação via headers)
│   └── gateway/
│       ├── api-reference.mdx
│       ├── authentication.mdx
│       ├── environments.mdx
│       ├── errors.mdx
│       ├── introduction.mdx
│       ├── pix-cash-in.mdx
│       ├── pix-cash-out.mdx
│       ├── pix-refund.mdx
│       ├── pix-status.mdx
│       └── webhooks.mdx
└── v2/                      # Documentação da API v2 (autenticação via Bearer token)
    └── gateway/
        ├── api-reference.mdx
        ├── authentication.mdx
        ├── environments.mdx
        ├── errors.mdx
        ├── introduction.mdx
        ├── pix-cash-in.mdx
        ├── pix-cash-out.mdx
        ├── pix-refund.mdx
        ├── pix-status.mdx
        └── webhooks.mdx
```

## ⚙️ Configuração do Projeto

O arquivo `docs.json` contém as configurações principais do projeto, incluindo:

- Tema e cores personalizadas
- Configuração da API para testes interativos
- Estrutura de navegação com versões v1 e v2
- Links para redes sociais e suporte

## 🔄 Versões da API

### API v1
- Autenticação via headers **ci** e **cs**
- Endpoints com prefixo `/api/v1/gateway/`
- Formato direto para integrações rápidas

### API v2
- Autenticação via **Bearer token**
- Endpoints com prefixo `/api/v2/gateway/`
- Mesmo conjunto de funcionalidades, com método de autenticação alternativo

## 🔌 Endpoints Principais

| Endpoint | Descrição |
|----------|------------|
| `/api/vX/gateway/pix/cash-in` | Recebimento de pagamentos via PIX |
| `/api/vX/gateway/pix/cash-out` | Envio de pagamentos via PIX |
| `/api/vX/gateway/pix/refund` | Estorno de pagamentos PIX |
| `/api/vX/gateway/pix/status` | Consulta de status de transações |

## 🔔 Webhooks

O sistema de webhooks permite receber notificações em tempo real sobre eventos relacionados às transações:

- Pagamentos recebidos
- Transferências realizadas
- Estornos processados
- Alterações de status

## 🛠️ Ferramentas Utilizadas

- [Mintlify](https://mintlify.com/) - Framework para documentação
- [OpenAPI/Swagger](https://swagger.io/) - Especificação da API
- [MDX](https://mdxjs.com/) - Markdown estendido para componentes interativos

## 📞 Suporte

Para dúvidas ou suporte técnico, entre em contato através do email: [suporte@relaxpay.app](mailto:suporte@relaxpay.app)

## 🔗 Links Úteis

- [Dashboard RelaxPay](https://dashboard.relaxpay.app)
- [Status do Serviço](https://status.relaxpay.app)
- [GitHub](https://github.com/relaxpay)
- [X/Twitter](https://twitter.com/relaxpay)
