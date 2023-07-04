---
description: API de assinatura de plano.
---

# Assinatura

{% swagger method="post" path="/signature" baseUrl="{URL}/api" summary="Criar uma assinatura vinculado ao usuário logado. " %}
{% swagger-description %}
Por padrão, é criado uma assinatura de plano para o usuário logado.
{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" required="true" %}
Bearer 

_token_
{% endswagger-parameter %}

{% swagger-parameter in="body" name="planId" type="Integer" required="true" %}
ID do plano
{% endswagger-parameter %}

{% swagger-parameter in="body" name="startDate" type="Date" required="true" %}
Data de inicio
{% endswagger-parameter %}

{% swagger-parameter in="body" name="endDate" type="Date" required="true" %}
Data de fim
{% endswagger-parameter %}

{% swagger-parameter in="body" name="payment_method" type="String" required="true" %}
Método de pagamento. Vejas os 

[codigos de cada método](assinatura.md#metodos-de-pagamento)


{% endswagger-parameter %}

{% swagger-parameter in="body" name="Status" %}
Status da assinatura. Veja os satatus 

[aqu](assinatura.md#status)

i. 
{% endswagger-parameter %}
{% endswagger %}

### Métodos de Pagamento&#x20;

<table data-full-width="false"><thead><tr><th>code</th><th>Metodos de Pagamento</th></tr></thead><tbody><tr><td>1</td><td>Boleto</td></tr><tr><td>2</td><td>Cartão Debito</td></tr><tr><td>3</td><td>Cartão Crédito</td></tr><tr><td>4</td><td>Pix</td></tr><tr><td>5</td><td>Transferência </td></tr></tbody></table>

### Status

<table data-full-width="false"><thead><tr><th>code</th><th>Status</th></tr></thead><tbody><tr><td>0</td><td>Pendente</td></tr><tr><td>1</td><td>Aprovado</td></tr><tr><td>2</td><td>Cancelado</td></tr><tr><td>3</td><td>Estorno</td></tr><tr><td>4</td><td>Solicitação de cancelamento</td></tr></tbody></table>

