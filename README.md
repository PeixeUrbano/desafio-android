# Avaliação para Engenheiro de Software Android

### Objetivo

O objetivo do teste é desenvolver um app que liste ofertas disponíveis próximas de um usuário e, conforme sua movimentação e após um período de tempo atualize as ofertas na interface.


### Requisitos do teste

* Utilize Android Studio IDE.
* Opcional Java ou Kotlin.
* Seja clean e teste sempre que possível.
* Bom gosto crítico visual fará muita diferença.
* Crie um projeto privado no Github e faça um push. * Crie uma pasta com o último apk release gerado e nos comunique por email.

### Instruções

Para resolver este problema será necessário:

* Uma splash com 5 segundos de cooldown com ícone de carregamento para apresentação das suas identificações. (nome, email, profissão, …)

* Uma tela com uma lista de ofertas onde cada oferta clicável deve expor um thumbnail da sua imagem, o título da oferta, a descrição da oferta e o preço.
	
    A lista deve ser chamada através da seguinte api pública:

```
https://api.peixeurbano.com.br/v3/deals?appSecret=QasVmHaL55PPbMvPiDJe&lat=X&lng=Y&refLat=X&refLng=Y&offset=0&limit=50&w=408&h=264&w_thumb=192&h_thumb=123 
```

> _Nota: X e Y são suas respectivas coordenadas_


- Thumbnail: r`esponse.images[k].image` 
- Título da oferta: `response.partner.name`
- Descrição: `response.short_title`   /   Preço: `response.sale_price`
- A lista de ofertas deve ser rolável e o parâmetro offset deve aumentar de `10` em `10` de forma a não impactar a fluidez da rolagem.
