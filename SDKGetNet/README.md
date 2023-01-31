### GETNET SDK PHP - API v1
E-commerce

Todos os passos e processos referentes à integração com o sistema de captura e autorização de transações financeiras da Getnet via as funcionalidades da API.

 Documentação oficial
* https://api.getnet.com.br/v1/doc/api

#### Composer
```
$ composer require kennedymistrineirodev/sdkgetnet
```

### Possíveis status de resposta de uma transação
|Status|Descrição|
| ------- | --------- |
|PENDING|Registrada ou Aguardando ação|
|CANCELED|Desfeita ou Cancelada|
|APPROVED|Aprovada|
|DENIED|Negada|
|AUTHORIZED|Autorizada pelo emissor|
|CONFIRMED|Confirmada ou Capturada|

### Cartões para testes

|  N. Cartão |  Resultado esperado |
| ------------ | ------------ |
|  5155901222280001 (Master)	  | Transação Autorizada  |
| 5155901222270002   (Master)|  Transação Não Autorizada |
|  5155901222260003 (Master) |  Transação Não Autorizada |
| 5155901222250004 (Master) |Transação Não Autorizada|
| 4012001037141112 (Visa) |Transação Autorizada|


### Ambientes disponíveis
|Paramentro|Detalhe|
| ------- | --------- |
|SANDBOX|Sandbox - para desenvolvedores |
|HOMOLOG|Homologação - para lojistas e devs |
|PRODUCTION|Produção - somente lojistas |

### Meios de Pagamento
|Modalidade|Descrição|
| ------- | --------- |
|CREDIT|Pagamento com cartão de crédito|
|DEBIT|Pagamento com cartão de débito|
|BOLETO|Gera boleto|


### Métodos de Pagamento
|Método|Descrição|
| ------- | --------- |
|Authorize|Autoriza uma transação com Pre-Auth ou não|
|AuthorizeConfirm|Confirma uma autorização de crédito|
|AuthorizeConfirmDebit|Confirma uma autorização de débito|
|AuthorizeCancel|Cancela a transação|
|Boleto|Gera boleto|