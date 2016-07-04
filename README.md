# Modules for work with parameters and client

## Settings

Database settings here: `lib/config/database.yml`

## Install dependensies

```
bundle install
```

## Migrate database

```
rake db:migrate
```

## How to use

Firstly in your script:
```
require './lib/outsoft.rb'
```

All methods for work with parameters here `lib/outsoft/params.rb`
To create parameter in root level:
```
    Outsoft::Params.add(name: name, value_type: value_type, value: value, label: label, company_id: company_id
```

To create parameter in nested level:
```
    Outsoft::Params.add_by_path(name: name, value_type: value_type, value: value, label: label, company_id: company_id
```

To update params:
```
    Outsoft::Params.add_by_path(name: name, value_type: value_type, value: value, label: label, company_id: company_id
```

To remove params:
```
    Outsoft::Params.add_by_path(name: name, value_type: value_type, value: value, label: label, company_id: company_id
```


All methods for work with clients here `lib/outsoft/clients.rb`. 
It has method `create`, to create client:
```
      Outsoft::Clients.create data: { id: 1 }
      Outsoft::Clients.create data: { id: 2, extra: [['exists_param', 'some value']] }
```

To update clients:
```
Outsoft::Clients.update id: id, predefined: predefined, extra: extra

```