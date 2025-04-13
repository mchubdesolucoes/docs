# RelaxPay Documentation

Documentação oficial da API RelaxPay, um gateway de pagamento moderno e intuitivo para integração de PIX.

<img src="./images/hero.png" alt="RelaxPay API" width="800" />

## 🚀 Recursos Implementados

| Recurso | Descrição |
|---------|-----------|
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
├── api/                     # Especificação OpenAPI
│   └── openapi.yaml        # Definição da API no formato OpenAPI
├── gateway/                 # Documentação principal da API
│   ├── authentication.mdx  # Autenticação na API
│   ├── environments.mdx    # Ambientes de desenvolvimento e produção
│   ├── pix-cash-in.mdx     # Recebimento de pagamentos PIX
│   ├── pix-cash-out.mdx    # Envio de pagamentos PIX
│   ├── webhooks.mdx        # Sistema de notificações
│   └── errors.mdx          # Códigos de erro e soluções
├── images/                  # Imagens utilizadas na documentação
├── api-reference.mdx        # Referência completa com exemplos de código
├── api-endpoints.mdx        # Lista detalhada dos endpoints disponíveis
├── api-playground.mdx       # Playground interativo para testar a API
├── introduction.mdx         # Página de boas-vindas e visão geral
├── docs.json                # Configuração do Mintlify
└── README.md                # Informações sobre o projeto
```

## ⚙️ Configuração do Projeto

O arquivo `docs.json` contém as configurações principais do projeto:

```json
{
  "$schema": "https://mintlify.com/docs.json",
  "theme": "mint",
  "name": "RelaxPay",
  "colors": {
    "primary": "#8b5cf6",
    "light": "#9e77f7",
    "dark": "#7a43f3"
  },
  "favicon": "/favicon.svg",
  "api": {
    "mdx": {
      "server": "https://sandbox.ws.relaxpay.site",
      "auth": {
        "method": "key"
      }
    }
  },
  "navigation": {
    "tabs": [
      {
        "tab": "Documentação",
        "groups": [
          {
            "group": "Introdução",
            "pages": [
              "introduction",
              "gateway/authentication",
              "gateway/environments"
            ]
          },
          {
            "group": "Gateway PIX",
            "pages": [
              "gateway/pix-cash-in",
              "gateway/pix-cash-out",
              "gateway/webhooks",
              "gateway/errors"
            ]
          }
        ]
      },
      {
        "tab": "Referência da API",
        "groups": [
          {
            "group": "Visão Geral",
            "pages": [
              "api-reference/introduction",
              "api-reference/authentication"
            ]
          },
          {
            "group": "PIX",
            "pages": [
              "api-reference/pix/reference",
              "api-reference/pix/cash-in",
              "api-reference/pix/cash-out",
              "api-reference/pix/examples"
            ]
          },
          {
            "group": "Webhooks",
            "pages": [
              "api-reference/webhooks/reference",
              "api-reference/webhooks/events",
              "api-reference/webhooks/examples"
            ]
          },
          {
            "group": "Erros",
            "pages": [
              "api-reference/errors"
            ]
          }
        ]
      },
      {
        "tab": "Playground",
        "groups": [
          {
            "group": "Testar API",
            "pages": [
              "playground/index",
              "playground/pix-cash-in",
              "playground/pix-cash-out",
              "playground/webhooks"
            ]
          }
        ]
      },
      {
        "tab": "OpenAPI",
        "openapi": "api/openapi.yaml"
      }
    ]
  }
}
```

## 🔌 Playground da API

A documentação inclui um playground interativo que permite:

- **Teste Real**: Experimente os endpoints diretamente no navegador
- **Visual Intuitivo**: Interface amigável para construir requisições
- **Visualização de Respostas**: Veja os resultados das chamadas formatados
- **Exploração de Parâmetros**: Entenda todas as opções disponíveis

Para utilizar o playground:

1. Acesse a página "Playground da API" na documentação
2. Insira suas credenciais de sandbox (Client ID e Client Secret)
3. Selecione o endpoint desejado
4. Preencha os parâmetros necessários
5. Clique em "Enviar" para testar a requisição

## 🖼️ Imagens

As imagens na pasta `/images/` são placeholders e devem ser substituídas por imagens reais antes da publicação. Sugerimos a criação das seguintes imagens:

- `auth-dashboard.png` - Tela do dashboard de obtenção de credenciais
- `webhooks-flow.png` - Diagrama do fluxo de webhooks
- `pix-cash-in-flow.png` - Diagrama do fluxo de PIX Cash-in
- `pix-cash-out-flow.png` - Diagrama do fluxo de PIX Cash-out
- `auth-flow.png` - Diagrama do fluxo de autenticação
- `ip-management.png` - Tela de gerenciamento de IPs autorizados

## 👥 Contribuição

1. Faça um fork do repositório
2. Crie uma branch para sua feature (`git checkout -b feature/nova-feature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/nova-feature`)
5. Abra um Pull Request

## 📞 Suporte

Para suporte, entre em contato:
📧 **suporte@relaxpay.app**

## Estrutura da API

A API RelaxPay está disponível em duas versões:

### API v1 (Versão Atual)
- Autenticação via headers `ci` e `cs`
- Endpoints com prefixo `/api/v1/gateway/`
- Documentação em `/v1/gateway/`

### API v2 (Nova Versão)
- Autenticação exclusivamente via Bearer token
- Endpoints com prefixo `/api/v2/gateway/`
- Inclui endpoint de autenticação para obter o token: `/api/v2/auth/token`
- Documentação em `/v2/gateway/`

Ambas as versões oferecem as mesmas funcionalidades, diferindo apenas no método de autenticação.
