# Migration and function mapping

## Source boundaries

| Classification | Result |
| --- | --- |
| Onetime only | One-time medical reserve, linked Saving withdrawal plan, retirement/life ages, premium adjustment, actual-pay calculation, reserve balance and actuarial outcome |
| Medsave only | Guided flow, management dashboards, Firebase media, GAS configuration and theme/personalisation; not imported |
| Similar | Medical premium inflation, preparation comparison and reserve presentation |
| Different calculation | Onetime projects premiums from a selected retirement age and offsets them with a one-time Saving plan; Medsave owns a different workflow and was not substituted |
| Preserved independently | Both original Onetime Sheet mappings, multiplier interpolation, premium fallback, extraction timing and net-outcome formula |

## Dependency result

Retirement Medical depends on Onetime's Saving rate and policy-value multiplier but not on its Saving UI. Those shared calculations were migrated into this module. It has no dependency on the removed fixed-deposit engine.

## Data and storage

The source feature has no LocalStorage, SessionStorage, IndexedDB, GAS writes or API writes. No migration is required. Both original public Google Sheet IDs and tab mappings remain unchanged.
