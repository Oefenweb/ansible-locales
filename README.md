## locales

[![Build Status](https://travis-ci.org/Oefenweb/ansible-locales.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-locales) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-locales-blue.svg)](https://galaxy.ansible.com/tersmitten/locales)

Set locales on Debian-like systems.

#### Requirements

None

#### Variables

 * `locales_present` [default: `[en_US.UTF-8]`]:
 * `locales_language_packs_present` [default: `[language-pack-en, language-pack-en-base]`]:
 * `locales_absent` [default: `[]`]:
 * `locales_language_packs_absent` [default: `[]`]:
 * `locales_default`:
   * `lang` [default: `[en_US.UTF-8]`]: Provides default value for LC_* variables that have not been explicitly set
   * `language` [optional]: Same as above? But with higher priority, [see](http://www.gnu.org/software/gettext/manual/gettext.html#Locale-Environment-Variables)
   * `lc_address` [optional]: How addresses are formatted (country first or last, where zip code goes etc.)
   * `lc_all` [optional]: Overrides individual LC_* settings: if LC_ALL is set, none of the below have any effect
   * `lc_collate` [optional]: How strings (file names...) are alphabetically sorted. Using the "C" or "POSIX" locale here results in a strcmp()-like sort order, which may be preferable to language-specific locales
   * `lc_ctype` [optional]: How characters are classified as letters, numbers etc. This determines things like how characters are converted between upper and lower case
   * `lc_identification` [optional]: Metadata about the locale information
   * `lc_measurement` [optional]: What units of measurement are used (feet, meters, pounds, kilos etc.)
   * `lc_messages` [optional]: What language should be used for system messages
   * `lc_monetary` [optional]: What currency you use, its name, and its symbol
   * `lc_name` [optional]: How names are represented (surname first or last, etc.)
   * `lc_numeric` [optional]: How you format your numbers. For example, in many countries a period (.) is used as a decimal separator, while others use a comma (,)
   * `lc_paper` [optional]: Paper sizes: 11 x 17 inches, A4, etc
   * `lc_response` [optional]: Determines how responses (such as Yes and No) appear in the local language
   * `lc_telephone` [optional]: What your telephone numbers look like
   * `lc_time` [optional]: How your time and date are formatted. Use for example "en_DK.UTF-8" to get a 24-hour-clock in some programs

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
    - locales
```

#### License

MIT

#### Author Information

Mischa ter Smitten (based on work of [knopki](https://github.com/knopki) and [nickjj](https://github.com/nickjj))

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-locales/issues)!
