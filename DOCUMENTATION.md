# Documentação Técnica

## Banco de Dados (Firebase Structure)
- `/users/{username}`: Armazena credenciais, roles, avatares e status de banimento.
- `/transportes/{id}`: Registros de motoristas, incluindo placas, fotos e geolocalização.
- `/chat/{room_id}`: Mensagens enviadas no sistema.

## Regras de Acesso (RBAC)
- `admin`: Acesso total (Gerenciamento + Portaria + Motorista).
- `portaria`: Acesso ao painel de liberação.
- `motorista`: Acesso ao formulário de entrada.

## Recursos Específicos
- **Geolocalização:** Capturada apenas no `motorista.html` e exibida exclusivamente no modal do `gerenciamento.html`.
- **Banimento:** Impede o login e encerra sessões ativas caso o campo `banned` seja true.
- **EricLM Tools:** Funções injetadas no escopo global para manutenção direta do Firebase (Limpeza de nós).