---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: true

  email: laparisidelannoy@uchicago.edu
  phone: (312)-394-9854
  address:
    street: 5757 S University Ave
    city: Chicago
    region: IL
    postcode: "60637"
    country: United States
    country_code: US
  coordinates:
    latitude: "41.789719"
    longitude: "-87.597219"
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: DM Me
      link: "https://twitter.com/LeoAparisidL"

design:
  columns: "2"
---
