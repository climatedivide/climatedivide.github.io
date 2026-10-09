---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        The New Climate Divide
        Research Group
      image:
        filename: logo_network.svg
      text: |
        <br>
        The research project focuses on the analysis of polarization around climate change as a political mobilization issue, shaped by an emerging right-wing front and an increasingly mainstream yet fragmented green camp.  

  - block: markdown
    content:
      title: Project Description
      subtitle: ''
      text: |
        The <b>New Climate Divide</b> project, financed by the <i>DFG Emmy Noether Programme</i>, asks how climate change is transforming from a broadly consensual issue into a *polarising political divide* that reshapes mobilisation, participation, and political identities in Europe. It theorises climate politics as a *distributive conflict* in which competing coalitions mobilise relative winners and losers through different problem definitions, policy visions, and reform trajectories, especially under conditions of overlapping economic and geopolitical crises. Empirically, the project investigates these dynamics across electoral and civil-society arenas in seven European countries between 2010 and 2030. 
        
        In three inter-related work packages, ClimateDivide examines how actors mobilise around climate change, how citizens engage in response, and how in-group and out-group identities emerge around the climate divide.
    design:
      columns: '1'

  - block: portfolio
    content:
      title: Work Packages
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
      title: Latest News
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
      title: Latest Publications
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
      title: Meet the Team
      subtitle: ''
      user_groups:
        - Principal Investigator
        - Postdoctoral Researcher
        - Researchers
        - Student Assistants
        - Administrative Assistance
      sort_by: Params.last_name
      sort_ascending: true
    design:
      show_social: true
      show_interests: false
      show_role: true
      show_organizations: true
---
