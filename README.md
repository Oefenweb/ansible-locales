## locales

[![CI](https://github.com/Oefenweb/ansible-locales/workflows/CI/badge.svg)](https://github.com/Oefenweb/ansible-locales/actions?query=workflow%3ACI)
[![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-locales-blue.svg)](https://galaxy.ansible.com/Oefenweb/locales)

Set locales on Debian-like systems.

#### Requirements

None

#### Variables

* `locales_present` [default: `['en_US.UTF-8']`]:
* `locales_absent` [default: `[]`]:
*
* `locales_language_packs_present` [default: `['language-pack-en', 'language-pack-en-base']`]:
* `locales_language_packs_absent` [default: `[]`]:
*
* `locales_default`: [default: `{}`]: Default declarations
* `locales_default.lang`: [default: `'en_US.UTF-8'`]: Provides default value for `LC_*` variables that have not been explicitly set
* `locales_default.language`: [optional]: Same as above? But with higher priority, [see](http://www.gnu.org/software/gettext/manual/gettext.html#Locale-Environment-Variables)
* `locales_default.lc_address`: [optional]: How addresses are formatted (country first or last, where zip code goes etc.)
* `locales_default.lc_all`: [optional]: Overrides individual `LC_*` settings: if `LC_ALL` is set, none of the below have any effect
* `locales_default.lc_collate`: [optional]: How strings (file names...) are alphabetically sorted. Using the "C" or "POSIX" locale here results in a strcmp()-like sort order, which may be preferable to language-specific locales
* `locales_default.lc_ctype`: [optional]: How characters are classified as letters, numbers etc. This determines things like how characters are converted between upper and lower case
* `locales_default.lc_identification`: [optional]: Metadata about the locale information
* `locales_default.lc_measurement`: [optional]: What units of measurement are used (feet, meters, pounds, kilos etc.)
* `locales_default.lc_messages`: [optional]: What language should be used for system messages
* `locales_default.lc_monetary`: [optional]: What currency you use, its name, and its symbol
* `locales_default.lc_name`: [optional]: How names are represented (surname first or last, etc.)
* `locales_default.lc_numeric`: [optional]: How you format your numbers. For example, in many countries a period (.) is used as a decimal separator, while others use a comma (,)
* `locales_default.lc_paper`: [optional]: Paper sizes: 11 x 17 inches, A4, etc
* `locales_default.lc_response`: [optional]: Determines how responses (such as Yes and No) appear in the local language
* `locales_default.lc_telephone`: [optional]: What your telephone numbers look like
* `locales_default.lc_time`: [optional]: How your time and date are formatted. Use for example "en_DK.UTF-8" to get a 24-hour-clock in some programs

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - oefenweb.locales
```

#### License

MIT

#### Author Information

Mischa ter Smitten (based on work of [knopki](https://github.com/knopki) and [nickjj](https://github.com/nickjj))

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-locales/issues)!
