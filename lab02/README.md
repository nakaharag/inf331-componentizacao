# Lab 02

## Tarefa sobre catálogo de componentes

[Link para o notebook](notebook/multiplas-interfaces.ipynb)

## Tarefa Web Components 1
```
<dcc-trigger label="Mundo" action="noticia/mundo/politica" value="Mundo P"></dcc-trigger>

<dcc-trigger label="Brasil P" action="noticia/brasil/politica" value="Brasil P"></dcc-trigger>

<dcc-trigger label="Brasil E" action="noticia/brasil/esporte" value="Brasil E"></dcc-trigger>

<dcc-trigger label="Bahia" action="noticia/brasil/bahia/esporte" value="Bahia E"></dcc-trigger>
<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Noticia: ">
  <subscribe-dcc topic="noticia/#/politica"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="Noticia: ">
  <subscribe-dcc topic="noticia/brasil/#"></subscribe-dcc>
</dcc-lively-talk>
<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="Noticia: ">
  <subscribe-dcc topic="noticia/#"></subscribe-dcc>
</dcc-lively-talk>
```

## Tarefa Web Components 2
```
<dcc-trigger label="Next Science Item" action="next/science/rss">
</dcc-trigger>

<dcc-trigger label="Next Design Item" action="next/design/rss">
</dcc-trigger>

<dcc-rss publish="rss/design" source="https://www.wired.com/category/design/feed">
  <subscribe-dcc topic="next/design/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-rss publish="rss/science" source="https://www.wired.com/category/science/feed">
  <subscribe-dcc topic="next/science/rss" role="step"></subscribe-dcc>
</dcc-rss>

<dcc-aggregator publish="aggregate/science" quantity="3">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-aggregator>

<dcc-lively-talk id="doctor"
                 duration="0s"
                 character="doctor"
                 speech="Aggregate Science (3): ">
  <subscribe-dcc topic="aggregate/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="nurse"
                 duration="0s"
                 character="nurse"
                 speech="Science ">
  <subscribe-dcc topic="rss/science"></subscribe-dcc>
</dcc-lively-talk>

<dcc-lively-talk id="patient"
                 duration="0s"
                 character="patient"
                 speech="Design: ">
  <subscribe-dcc topic="rss/design"></subscribe-dcc>
</dcc-lively-talk>
```