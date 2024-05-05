---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  # - block: skills
  #   content:
  #     title: Skills
  #     text: ''
  #     # Choose a user to display skills from (a folder name within `content/authors/`)
  #     username: admin
    # design:
    #   columns: '1'
  - block: experience
    id: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items: 
        - title: Researcher
          company: RISE Research Institutes of Sweden
          company_url: ''
          company_logo: rise
          location: Sweden
          date_start: '2023-08-01'
          date_end: ''
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: Lecturer
          company: Chalmers University of Technology
          company_url: ''
          company_logo: chalmers
          location: Sweden
          date_start: '2023-10-01'
          date_end: ''
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: PhD Student
          company: University of Gothenburg
          company_url: ''
          company_logo: gu
          location: Sweden
          date_start: '2018-06-01'
          date_end: '2023-08-01'
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: Business Analyst
          company: Volvo Cars
          company_url: ''
          company_logo: volvo
          location: Sweden
          date_start: '2016-08-01'
          date_end: '2018-06-01'
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: IT Consultant
          company: ALTEN Sweden
          company_url: ''
          company_logo: alten
          location: Sweden
          date_start: '2016-07-01'
          date_end: '2018-06-01'
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: Oracle Database Administrator
          company: Syriatel
          company_url: ''
          company_logo: syriatel
          location: Syria
          date_start: '2013-02-01'
          date_end: '2014-08-01'
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: System Analyst
          company: TeachArabia
          company_url: ''
          company_logo: techarabia
          location: Syria
          date_start: '2012-09-01'
          date_end: '2013-01-01'
        - title: Development Team Lead
          company: Bank of Syria and Overseas
          company_url: ''
          company_logo: bank
          location: Syria
          date_start: '2010-07-01'
          date_end: '2012-12-01'
          # description: Taught electronic engineering and researched semiconductor physics.
        - title: Development specialist
          company: Syriatel
          company_url: ''
          company_logo: syriatel
          location: Syria
          date_start: '2007-12-01'
          date_end: '2010-07-01'
          # description: |2-
          #     Responsibilities include:

          #     * Analysing
          #     * Modelling
          #     * Deploying
        
    design:
      columns: '2'
  - block: accomplishments
    id: projects
    content:
      # Note: `&shy;` is used to add a 'soft' hyphen in a long heading.
      title: 'Projects'
      subtitle:
      # Date format: https://docs.hugoblox.com/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `item` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - certificate_url: ''
          date_end: ''
          date_start: '2022-08-01'
          description: ''
          icon: ''
          organization: '' 
          organization_url: ''
          title: AGRARSENSE
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2023-03-01'
          description: ''
          icon: ''
          organization: ''
          organization_url: ''
          title: EVIDENT
          url: ''
        - certificate_url: ''
          date_end: ''
          date_start: '2023-03-01'
          description: ''
          icon: ''
          organization: ''
          organization_url: ''
          title: 'CASUS: Building Security Assurance Cases in Automotive Open Systems'
          url: ''

    design:
      columns: '2'
  # - block: collection
  #   id: posts
  #   content:
  #     title: Recent Posts
  #     subtitle: ''
  #     text: ''
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       folders:
  #         - post
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: compact
  #     columns: '2'
  # - block: portfolio
  #   id: projects
  #   content:
  #     title: Projects
  #     filters:
  #       folders:
  #         - project
  #     # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
  #     default_button_index: 0
  #     # Filter toolbar (optional).
  #     # Add or remove as many filters (`filter_button` instances) as you like.
  #     # To show all items, set `tag` to "*".
  #     # To filter by a specific tag, set `tag` to an existing tag name.
  #     # To remove the toolbar, delete the entire `filter_button` block.
  #     buttons:
  #       - name: All
  #         tag: '*'
  #       - name: Deep Learning
  #         tag: Deep Learning
  #       - name: Other
  #         tag: Demo
  #   design:
  #     # Choose how many columns the section has. Valid values: '1' or '2'.
  #     columns: '1'
  #     view: showcase
  #     # For Showcase view, flip alternate rows?
  #     flip_alt_rows: false
  # - block: markdown
  #   content:
  #     title: Gallery
  #     subtitle: ''
  #     text: |-
  #       {{< gallery album="demo" >}}
  #   design:
  #     columns: '1'
  # - block: collection
  #   id: featured
  #   content:
  #     title: Featured Publications
  #     filters:
  #       folders:
  #         - publication
  #       featured_only: true
  #   design:
  #     columns: '2'
  #     view: card
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     columns: '2'
  #     view: compact
  # - block: tag_cloud
  #   content:
  #     title: Popular Topics
  #   design:
  #     columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
       You are welcome to reach out if you have any questions or inquiries.
      # Contact (add or remove contact options as necessary)
      email: m****.mo*****(at)ri.se
      address:
        street: Brinellgatan 4
        city: Borås
        postcode: '504 62'
        country: Sweden
      # directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
      # office_hours:
      #   - 'Monday 10:00 to 13:00'
      #   - 'Wednesday 09:00 to 10:00'
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '57.716948740940104'
        longitude: '12.892886242329457'  
      # contact_links:
      #   - icon: twitter
      #     icon_pack: fab
      #     name: DM Me
      #     link: 'https://twitter.com/Twitter'
  
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---
