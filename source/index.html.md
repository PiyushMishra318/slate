---
title: API Documentation

language_tabs: # must be one of https://git.io/vQNgJ
  - shell
  - ruby
  - python
  - javascript

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>


search: true
---

# Introduction

Welcome to the Greasy Monkey  API! You can use our API to access Greasy Monkey API endpoints, which can help you to build and integrate frontend and backend efficiently.

We have language bindings in Shell, Ruby, Python, and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

#Customer

##Cars

###Create/Add
This Api is used to add customers cars.
<br>
### HTTP Request
`POST customer/car/create`
###Sample Body Format

{<br>
   {<br>
    customer: 'Customer id',<br>
    brand: 'TATA',<br>
    model_name: 'Sumo',<br>
    model_variant: 'Diesel',<br>
    model_year: '2009',<br>
    overview: {<br>
      engine_oil: {<br>
        type: false,<br>
        default: true<br>
      },<br>
      tier: {<br>
        type: false,<br>
        default: true<br>
      },<br>
      suspension: {<br>
        type: false,<br>
        default: true<br>
      },<br>
      brakes: {<br>
        type: false,<br>
        default: true<br>
      },<br>
      electrical_checkup: {<br>
        type: false,<br>
        default: true<br>
      },<br>
      air_conditioner: {<br>
        type: true,<br>
        default: true<br>
      }<br>
    },<br>
    fuel_type: 'Petrol'<br>
  },<br>
  {<br>
    timestamps: true<br>
  }<br>
}<br>
