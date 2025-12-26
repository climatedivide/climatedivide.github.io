---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        Die neue klimapolitische Spaltung
        Forschungsgruppe
      image:
        filename: logo_network.svg
      text: |
        <br>
        Das Forschungsprojekt untersucht die Polarisierung rund um den Klimawandel als politisches Mobilisierungsthema, geprägt von einer sich formierenden rechten Front und einem zunehmend mainstreamigen, aber fragmentierten grünen Lager.

  - block: markdown
    content:
      title: Projektbeschreibung
      subtitle: ''
      text: |
        Das Projekt <b>Die neue klimapolitische Spaltung</b>, finanziert durch das <i>DFG-Emmy-Noether-Programm</i>, fragt, wie sich der Klimawandel von einem weitgehend konsensualen Thema zu einer *polarisierenden politischen Konfliktlinie* entwickelt, die Mobilisierung, Teilhabe und politische Identitäten in Europa verändert. Es versteht Klimapolitik als *Verteilungskonflikt*, in dem konkurrierende Koalitionen relative Gewinner:innen und Verlierer:innen über unterschiedliche Problemdefinitionen, Politikvisionen und Reformpfade mobilisieren – insbesondere unter Bedingungen sich überlagernder wirtschaftlicher und geopolitischer Krisen. 
        
        In drei miteinander verknüpften Arbeitspaketen untersucht ClimateDivide, wie Akteur:innen zum Thema Klimawandel mobilisieren, wie Bürger:innen darauf reagieren und wie sich Zugehörigkeits- und Abgrenzungsidentitäten entlang der Klimafrage herausbilden.
    design:
      columns: '1'

  - block: portfolio
    content:
      title: Arbeitspakete
      filters:
        folders:
          - project
      sort_by: weight
      sort_ascending: true
    design:
      view: masonry
      columns: '1'
      css_class: focus-areas

  - block: collection
    content:
      title: Neueste Meldungen
      count: 5
      filters:
        folders:
          - news
        exclude_featured: false
        exclude_future: false
      sort_by: Date
      sort_ascending: false
    design:
      view: compact
      columns: '1'
      css_class: news-list
  
  - block: collection
    content:
      title: Aktuelle Publikationen
      text: ""
      count: 5
      filters:
        folders:
          - publication
      sort_by: Date
      sort_ascending: false
    design:
      view: citation
      columns: '1'

  - block: people
    content:
      title: Team kennenlernen
      subtitle: ''
      user_groups:
        - Projektleitung
        - Postdoktorand:innen
        - Forschende
        - Studentische Hilfskräfte
        - Administrative Assistenz
      sort_by: Params.last_name
      sort_ascending: true
    design:
      show_social: true
      show_interests: false
      show_role: true
      show_organizations: true
---
