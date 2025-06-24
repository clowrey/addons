# Changelog

## [8.0.2] - 2024-12-19

### Changed
- **BREAKING**: Modified addon to work exclusively on `/config/esphome` subdirectory instead of entire `/config` directory
- Updated addon name to "Git pull (ESPHome)" to reflect focused purpose
- Changed all git operations to work within `/config/esphome` directory only
- Updated backup functionality to only backup esphome directory contents
- Modified log messages throughout to reflect esphome-specific operations
- Updated documentation to clarify addon only affects ESPHome configuration files
- Changed default `restart_ignore` examples from Home Assistant files to ESPHome-relevant patterns
- Added automatic creation of `/config/esphome` directory if it doesn't exist

### Added
- Enhanced safety warnings in documentation to clarify only ESPHome configs are affected
- Added note in documentation that other Home Assistant configuration files remain untouched
- Added informational log message indicating addon is configured for esphome subdirectory only

### Migration Notes
- **Important**: This version only manages files in `/config/esphome/` 
- Users who previously used this addon for full configuration management should use the original addon
- ESPHome users can now safely use this addon without affecting their main Home Assistant configuration
- Repository should now point to an ESPHome-specific configuration repository

## [8.0.1] - Previous Version
- Original functionality for full `/config` directory management

## 8.0.0
- Refactor git_pull to use HA Api with bashio
- Update base image to Alpine 3.21
- Remove ha cli dependency


## 7.14.1
- Fix error where $HOME is not defined

## 7.14.0

- Update base image to Alpine 3.19
- Update Home Assistant CLI to 4.31.0

## 7.13.1

- Update Home Assistant CLI to 4.12.2

## 7.13.0

- Update Home Assistant CLI to 4.12.1
- Upgrade base image to Alpine 3.13
- Supress a shellcheck warning happening in CI

## 7.12.2

- Update Home Assistant CLI to 4.11.0

## 7.12.1

- Update options schema for passwords

## 7.12.0

- Fix error of deployment_key eventually failing by overwriting the deployment_key every cycle

## 7.11.0

- Update Home Assistant CLI to 4.2.0

## 7.10.0

- Update Home Assistant CLI to 4.1.0

## 7.9.0

- Update Home Assistant CLI to 4.0.1

## 7.8.0

- Added support for Azure DevOps repositories by removing the requirement for the `.git` suffix
- Update to Alpine 3.11

## 7.7.0

- Update Hass.io CLI to 3.1.1

## 7.6.0

- Update Hass.io CLI to 3.1.0

## 7.5.0

- Update Hass.io CLI to 3.0.0

## 7.4.0

- Update Hass.io CLI to 2.3.0

## 7.3.0

- Update Hass.io CLI to 2.2.0

## 7.2.0

- Fix restart_ignore when specifying a sub-directory

## 7.1.0

- Enhance restart_ignore to support whole directories
- Fix repeat option: don't terminate if internet connection unavailable during a check

## 7.0.0

- Update Hass.io CLI to 2.0.1

## 6.1.0

- Bugfix in git diff command while comparing commits

## 6.0.0

- Allow to disable Home Assistant restart for specific file changes
