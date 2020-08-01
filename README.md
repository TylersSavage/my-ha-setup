# My Home Assistant Lovelace setup

This layout was designed mobile-first.

## Main view layout

<details><summary><b>Show code</b></summary>

```yaml
      - cards:
          - entities:
              - attribute: color_temp
                entity: light.desk_light
                haptic: success
                step: 15
                toggle: true
                type: 'custom:slider-entity-row'
              - entity: light.bedside_lamp
                haptic: success
                hide_when_off: true
                name: TV Lamp
                toggle: true
                type: 'custom:slider-entity-row'
            show_header_toggle: false
            type: entities
          - cards:
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: light.bedside_lamp_nightlight
                hold_action:
                  action: more-info
                icon: 'mdi:power-sleep'
                show_name: false
                size: 35%
                styles:
                  card:
                    - height: 56px
                tap_action:
                  action: toggle
                  haptic: success
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.lofi_beats
                hold_action:
                  action: more-info
                show_name: false
                size: 35%
                styles:
                  card:
                    - height: 56px
                tap_action:
                  action: toggle
                  haptic: success
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.lofi_beats2
                hold_action:
                  action: more-info
                icon: 'mdi:music-circle-outline'
                show_name: false
                size: 35%
                styles:
                  card:
                    - height: 56px
                tap_action:
                  action: toggle
                  haptic: success
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.jazz_radio
                hold_action:
                  action: more-info
                show_name: false
                size: 35%
                styles:
                  card:
                    - height: 56px
                tap_action:
                  action: toggle
                  haptic: success
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.circadian_lighting_circadian_lighting
                hold_action:
                  action: more-info
                show_name: false
                size: 35%
                styles:
                  card:
                    - height: 56px
                tap_action:
                  action: toggle
                  haptic: success
                type: 'custom:button-card'
            type: horizontal-stack
          - cards:
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.always_on_shutdown
                hold_action:
                  action: more-info
                icon: 'mdi:power'
                name: ALWAYS
                show_name: true
                size: 35%
                styles:
                  card:
                    - height: 56px
                    - font-size: 12px
                    - font-weight: bold
                tap_action:
                  action: none
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.always_on_restart
                hold_action:
                  action: more-info
                icon: 'mdi:restart'
                name: 'ON'
                show_name: true
                size: 35%
                styles:
                  card:
                    - height: 56px
                    - font-size: 12px
                    - font-weight: bold
                tap_action:
                  action: none
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.adguard_protection
                hold_action:
                  action: more-info
                show_name: false
                size: 35%
                styles:
                  card:
                    - height: 56px
                tap_action:
                  action: toggle
                  haptic: success
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.x200m_shutdown
                hold_action:
                  action: more-info
                icon: 'mdi:power'
                name: X200M
                show_name: true
                size: 35%
                styles:
                  card:
                    - height: 56px
                    - font-size: 12px
                    - font-weight: bold
                tap_action:
                  action: none
                type: 'custom:button-card'
              - color: auto
                color_type: card
                double_tap_action:
                  action: toggle
                  haptic: success
                entity: switch.x200m_restart
                hold_action:
                  action: more-info
                icon: 'mdi:restart'
                name: X200M
                show_name: true
                size: 35%
                styles:
                  card:
                    - height: 56px
                    - font-size: 12px
                    - font-weight: bold
                tap_action:
                  action: none
                type: 'custom:button-card'
            type: horizontal-stack
        type: vertical-stack
      - cards:
          - cards:
              - align_state: center
                animate: true
                color_thresholds:
                  - color: '#ff0000'
                    value: 80
                  - color: '#ff8600'
                    value: 50
                  - color: '#04e700'
                    value: 30
                decimals: 0
                entities:
                  - entity: sensor.processor_use
                    state_adaptive_color: true
                font_size: 105
                hours_to_show: 1
                icon: 'mdi:cpu-64-bit'
                line_width: 4
                name: CPU
                points_per_hour: 8
                show:
                  fill: false
                  icon_adaptive_color: true
                  labels: false
                  name_adaptive_color: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px
                    14px !important
                  }
                type: 'custom:mini-graph-card'
              - align_state: center
                animate: true
                color_thresholds:
                  - color: '#ff0000'
                    value: 95
                  - color: '#ff8600'
                    value: 97
                  - color: '#04e700'
                    value: 99
                entities:
                  - entity: sensor.internet_health
                    state_adaptive_color: true
                font_size: 105
                hours_to_show: 1
                line_width: 4
                name: Internet
                points_per_hour: 8
                show:
                  fill: false
                  icon_adaptive_color: true
                  labels: false
                  name_adaptive_color: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 16px 0 16px !important
                  }
                  ha-card > .info {
                    padding: 0 16px 0px 16px !important
                  }
                type: 'custom:mini-graph-card'
                upper_bound: 100.1
            type: horizontal-stack
          - default: idle
            entity: sensor.qbt_status
            states:
              downloading:
                cards:
                  - align_icon: state
                    animate: true
                    decimals: 0
                    entities:
                      - color: '#317ACC'
                        entity: sensor.qbt_down_speed
                        state_adaptive_color: true
                    hours_to_show: 1
                    icon: 'mdi:arrow-down'
                    line_width: 4
                    name: qBt Down
                    points_per_hour: 20
                    show:
                      fill: false
                      icon_adaptive_color: true
                      labels: false
                      legend: false
                      name: false
                      name_adaptive_color: true
                      points: false
                      state: true
                    style: |
                      ha-card > div:nth-child(-n+2) {
                        padding: 0 14px 0 14px !important
                      }
                      ha-card > .info {
                        padding: 0 14px 0px 14px !important
                      }
                    type: 'custom:mini-graph-card'
                    unit: KB/s
                  - align_icon: state
                    animate: true
                    decimals: 0
                    entities:
                      - color: '#317ACC'
                        entity: sensor.qbt_up_speed
                        state_adaptive_color: true
                    hours_to_show: 1
                    icon: 'mdi:arrow-up'
                    line_width: 4
                    name: qBt Up
                    points_per_hour: 20
                    show:
                      fill: false
                      icon_adaptive_color: true
                      labels: false
                      legend: false
                      name: false
                      name_adaptive_color: true
                      points: false
                      state: true
                    style: |
                      ha-card > div:nth-child(-n+2) {
                        padding: 0 14px 0 14px !important
                      }
                      ha-card > .info {
                        padding: 0 14px 0px 14px !important
                      }
                    type: 'custom:mini-graph-card'
                    unit: KB/s
                type: horizontal-stack
              idle:
                cards:
                  - entity: sensor.mergerfs
                    type: entity
                    unit: free
                  - entity: sensor.drive_used
                    icon: 'mdi:google-drive'
                    name: Google Drive
                    type: entity
                    unit: used
                type: horizontal-stack
              seeding:
                cards:
                  - align_icon: state
                    animate: true
                    decimals: 0
                    entities:
                      - color: '#F08B32'
                        entity: sensor.qbt_down_speed
                        state_adaptive_color: true
                    hours_to_show: 1
                    icon: 'mdi:arrow-down'
                    line_width: 4
                    name: qBt Down
                    points_per_hour: 20
                    show:
                      fill: false
                      icon_adaptive_color: true
                      labels: false
                      legend: false
                      name: false
                      name_adaptive_color: true
                      points: false
                      state: true
                    style: |
                      ha-card > div:nth-child(-n+2) {
                        padding: 0 14px 0 14px !important
                      }
                      ha-card > .info {
                        padding: 0 14px 0px 14px !important
                      }
                    type: 'custom:mini-graph-card'
                    unit: KB/s
                  - align_icon: state
                    animate: true
                    decimals: 0
                    entities:
                      - color: '#F08B32'
                        entity: sensor.qbt_up_speed
                        state_adaptive_color: true
                    hours_to_show: 1
                    icon: 'mdi:arrow-up'
                    line_width: 4
                    name: qBt Up
                    points_per_hour: 20
                    show:
                      fill: false
                      icon_adaptive_color: true
                      labels: false
                      legend: false
                      name: false
                      name_adaptive_color: true
                      points: false
                    style: |
                      ha-card > div:nth-child(-n+2) {
                        padding: 0 14px 0 14px !important
                      }
                      ha-card > .info {
                        padding: 0 14px 0px 14px !important
                      }
                    type: 'custom:mini-graph-card'
                    unit: KB/s
                type: horizontal-stack
              up_down:
                cards:
                  - align_icon: state
                    animate: true
                    decimals: 0
                    entities:
                      - color: '#317ACC'
                        entity: sensor.qbt_down_speed
                        state_adaptive_color: true
                    hours_to_show: 1
                    icon: 'mdi:arrow-down'
                    line_width: 4
                    name: qBt In
                    points_per_hour: 20
                    show:
                      fill: false
                      icon_adaptive_color: true
                      labels: false
                      name: false
                      name_adaptive_color: true
                      points: false
                    style: |
                      ha-card > div:nth-child(-n+2) {
                        padding: 0 14px 0 14px !important
                      }
                      ha-card > .info {
                        padding: 0 14px 0px 14px !important
                      }
                    type: 'custom:mini-graph-card'
                    unit: KB/s
                  - align_icon: state
                    animate: true
                    decimals: 0
                    entities:
                      - color: '#317ACC'
                        entity: sensor.qbt_up_speed
                        state_adaptive_color: true
                    hours_to_show: 1
                    icon: 'mdi:arrow-up'
                    line_width: 4
                    name: qBt Out
                    points_per_hour: 20
                    show:
                      fill: false
                      icon_adaptive_color: true
                      labels: false
                      legend: false
                      name: false
                      name_adaptive_color: true
                      points: false
                    style: |
                      ha-card > div:nth-child(-n+2) {
                        padding: 0 14px 0 14px !important
                      }
                      ha-card > .info {
                        padding: 0 14px 0px 14px !important
                      }
                    type: 'custom:mini-graph-card'
                    unit: KB/s
                type: horizontal-stack
            type: 'custom:state-switch'
          - card:
              type: entities
            filter:
              exclude:
                - state: 'off'
                - state: unavailable
                - state: standby
                - state: idle
                - entity_id: media_player.new_room_echo
              include:
                - domain: media_player
            show_empty: false
            sort:
              method: last_changed
            type: 'custom:auto-entities'
        type: vertical-stack  
```
</details>

## Info view

<details><summary><b>Show code</b></summary>

```yaml
      - cards:
          - cards:
              - align_state: left
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 4
                  - color: '#e1e700'
                    value: 2
                  - color: '#04e700'
                    value: 1
                decimals: 1
                entities:
                  - entity: sensor.load_1m
                    state_adaptive_color: false
                font_size: 85
                hours_to_show: 1
                line_width: 5
                name: 1-min
                points_per_hour: 12
                show:
                  fill: true
                  icon_adaptive_color: true
                  labels: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
              - align_icon: right
                align_state: left
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 4
                  - color: '#e1e700'
                    value: 3
                  - color: '#04e700'
                    value: 1
                decimals: 1
                entities:
                  - entity: sensor.load_5m
                    state_adaptive_color: false
                font_size: 85
                hours_to_show: 1
                line_width: 5
                name: 5-min
                points_per_hour: 12
                show:
                  fill: true
                  icon_adaptive_color: true
                  labels: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
              - align_icon: right
                align_state: left
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 4
                  - color: '#e1e700'
                    value: 3
                  - color: '#04e700'
                    value: 1
                decimals: 1
                entities:
                  - entity: sensor.load_15m
                    state_adaptive_color: false
                font_size: 85
                hours_to_show: 6
                line_width: 5
                name: 15-min
                points_per_hour: 2
                show:
                  fill: true
                  icon_adaptive_color: true
                  labels: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
            type: horizontal-stack
          - cards:
              - animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 250
                  - color: '#e1e700'
                    value: 150
                  - color: '#04e700'
                    value: 100
                decimals: 0
                entities:
                  - entity: sensor.adguard_average_processing_speed
                    state_adaptive_color: false
                font_size: 85
                hours_to_show: 3
                line_width: 5
                name: DNS
                points_per_hour: 4
                show:
                  fill: true
                  icon_adaptive_color: true
                  labels: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
              - animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 10
                  - color: '#e1e700'
                    value: 15
                  - color: '#04e700'
                    value: 20
                decimals: 1
                entities:
                  - entity: sensor.adguard_dns_queries_blocked_ratio
                    state_adaptive_color: false
                font_size: 85
                hours_to_show: 3
                line_width: 5
                name: Ads Blocked
                points_per_hour: 6
                show:
                  fill: true
                  icon_adaptive_color: true
                  labels: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
              - animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 75
                  - color: '#e1e700'
                    value: 40
                  - color: '#04e700'
                    value: 25
                decimals: 0
                entities:
                  - entity: sensor.disk_use_percent_home_agneev
                    state_adaptive_color: false
                font_size: 85
                hours_to_show: 6
                line_width: 5
                name: SSD
                points_per_hour: 3
                show:
                  fill: true
                  icon_adaptive_color: true
                  labels: false
                  name_adaptive_color: false
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
            type: horizontal-stack
          - cards:
              - card:
                  animate: true
                  color_thresholds:
                    - color: '#ff0000'
                      value: 80
                    - color: '#e1e700'
                      value: 65
                    - color: '#04e700'
                      value: 50
                  decimals: 0
                  entities:
                    - entity: sensor.cpu_temp
                      state_adaptive_color: false
                  font_size: 85
                  hours_to_show: 3
                  line_width: 3
                  name: '${ states[''sensor.throttled_state''].state }'
                  points_per_hour: 6
                  show:
                    fill: true
                    icon_adaptive_color: true
                    labels: false
                    name_adaptive_color: false
                    points: false
                  style: |
                    ha-card > div:nth-child(-n+2) {
                      padding: 0 14px 0 14px !important
                    }
                    ha-card > .info {
                      padding: 0 14px 0px 14px !important
                    }
                  type: 'custom:mini-graph-card'
                entities:
                  - sensor.throttled_state
                type: 'custom:config-template-card'
              - card:
                  animate: true
                  color_thresholds:
                    - color: '#ff0000'
                      value: 70
                    - color: '#e1e700'
                      value: 60
                    - color: '#04e700'
                      value: 55
                  decimals: 0
                  entities:
                    - entity: sensor.always_on_cpu_temp
                      state_adaptive_color: false
                  font_size: 85
                  hours_to_show: 3
                  line_width: 3
                  name: '${ states[''sensor.always_on_throttled_state''].state }'
                  points_per_hour: 6
                  show:
                    fill: true
                    icon_adaptive_color: true
                    labels: false
                    name_adaptive_color: false
                    points: false
                  style: |
                    ha-card > div:nth-child(-n+2) {
                      padding: 0 14px 0 14px !important
                    }
                    ha-card > .info {
                      padding: 0 14px 0px 14px !important
                    }
                  type: 'custom:mini-graph-card'
                entities:
                  - sensor.always_on_throttled_state
                type: 'custom:config-template-card'
            type: horizontal-stack
          - entities:
              - entity: sensor.eth0_in
              - entity: sensor.eth0_out
            hours_to_show: 1
            refresh_interval: 30
            type: history-graph
        type: vertical-stack
      - cards:
          - cards:
              - align_icon: state
                align_state: center
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 60
                  - color: '#e1e700'
                    value: 75
                  - color: '#04e700'
                    value: 95
                decimals: 0
                entities:
                  - entity: sensor.speedtest_net_download
                    state_adaptive_color: true
                hours_to_show: 6
                icon: 'mdi:arrow-down'
                line_width: 4
                name: ' '
                points_per_hour: 2
                show:
                  fill: false
                  icon: true
                  icon_adaptive_color: true
                  labels: false
                  legend: false
                  name: false
                  points: false
                  state: true
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
              - align_icon: state
                align_state: center
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 60
                  - color: '#e1e700'
                    value: 75
                  - color: '#04e700'
                    value: 95
                decimals: 0
                entities:
                  - entity: sensor.speedtest_net_upload
                    state_adaptive_color: true
                hours_to_show: 6
                icon: 'mdi:arrow-up'
                line_width: 4
                name: ' '
                points_per_hour: 2
                show:
                  fill: false
                  icon: true
                  icon_adaptive_color: true
                  labels: false
                  legend: false
                  name: false
                  points: false
                  state: true
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
            type: horizontal-stack
          - cards:
              - align_icon: state
                align_state: center
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 15
                  - color: '#e1e700'
                    value: 10
                  - color: '#04e700'
                    value: 5
                decimals: 0
                entities:
                  - entity: sensor.speedtest_net_ping
                    state_adaptive_color: true
                hours_to_show: 6
                line_width: 4
                name: Ping
                points_per_hour: 2
                show:
                  fill: false
                  icon_adaptive_color: true
                  labels: false
                  legend: false
                  name: true
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
              - align_icon: state
                align_state: center
                animate: false
                color_thresholds:
                  - color: '#ff0000'
                    value: 5
                  - color: '#e1e700'
                    value: 2
                  - color: '#04e700'
                    value: 1
                entities:
                  - entity: sensor.speedtest_net_jitter
                    state_adaptive_color: true
                hours_to_show: 6
                line_width: 4
                name: Jitter
                points_per_hour: 2
                show:
                  fill: false
                  icon_adaptive_color: true
                  labels: false
                  legend: false
                  name: true
                  points: false
                style: |
                  ha-card > div:nth-child(-n+2) {
                    padding: 0 14px 0 14px !important
                  }
                  ha-card > .info {
                    padding: 0 14px 0px 14px !important
                  }
                type: 'custom:mini-graph-card'
            type: horizontal-stack
          - entities:
              - entity: binary_sensor.operator
              - entity: binary_sensor.google_dns_ping
                name: Internet
            hours_to_show: 1
            refresh_interval: 30
            type: history-graph
          - cards:
              - entity: sensor.eth0_in_total
                type: entity
              - entity: sensor.eth0_out_total
                type: entity
            type: horizontal-stack
        type: vertical-stack
```
</details>

## Info 2 view 