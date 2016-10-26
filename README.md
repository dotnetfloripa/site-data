# Fonte de dados do DotNetFloripa.com
Este repositório controla os arquivos de fonte de dados para o site do [DotNetFloripa](http://www.dotnetfloripa.com/).

Quer ajudar a manter o site atualizado ou tem alguma vaga para publicar? Aqui é o lugar para isso!
Os arquivos são JSON e mais detalhes sobre a estrutura você encontra abaixo.

## Empresas
Inclua sua empresa na lista para que todos conheçam os players aqui da região!

Estrutura do arquivo `companies.json`:
```javascript
[
 {
  "Name": "Empresa 1"
  , "Description": "Descrição da empresa 1"
  , "Site": "http://site.empresa.1"
  , "Address": "Endereço empresa 1"
  , "LogoUrl": "http://link.logo.empresa.1"
 }
 , {
  "Name": "Empresa 2"
  , "Description": "Descrição da empresa 2"
  , "Site": "http://site.empresa.2"
  , "Address": "Endereço empresa 2"
  , "LogoUrl": "http://link.logo.empresa.2"
 }
]
```

Ou seja, é um `array` de objetos do tipo empresa. Recomendações:
- **Não esqueça as vírgulas**. Cada propriedade e cada objeto devem ser separados por vírgula.
- Recomendamos que sejam utilizadas aspas duplas porque alguma empresa pode ter aspa simples no seu nome.
- Logo deve ter no máximo **252x88 px**.

## Vagas
Quer anunciar uma vaga de .Net *aqui na região*? Ótimo! Inclua sua vaga no `jobs.json`, respeitando o seguinte formato:
```javascript
[
 {
  "Title": "Vaga 1"
  , "Description": "Descrição vaga 1."
  , "Opened": "2016-10-21"
  , "Closed": "2016-10-22"
  , "AnnouncedBy": "Pessoa ou empresa responsável pela vaga 1"
  , "Company": {
   "Name": "Empresa vaga 1"
   , "Site": "Site da empresa vaga 1"
  }
 }
 , {
  "Title": "Vaga 2"
  ...
  }
 }
]
``` 
Novamente, um `array` de objetos. Desta vez, vagas. Observações:
- `Closed` é opcional. Se deixar em branco, inclua aspas. Exemplo: `"Closed" : ""`
- Inclua uma data fim se o seu processo tiver um período determinado ou volte aqui no repo e informe quando foi encerrado. Não queremos manter vagas anunciadas que não estejam abertas de verdade!
- A descrição suporta HTML, fique à vontade para fazer algo bonito.
- O objeto `Company` não precisa ser completo. Recomendamos nome e site, pelo menos.

---

É isso aí! Clone o repo, faça suas alterações e submeta seu PR!