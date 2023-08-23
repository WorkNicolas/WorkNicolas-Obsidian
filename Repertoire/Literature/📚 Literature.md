---

database-plugin: basic

---

```yaml:dbfolder
name: 📚 Literature
description: Literature review database
columns:
  column1:
    input: text
    key: column1
    accessorKey: column1
    label: Column 1
    position: 0
    skipPersist: false
    isHidden: true
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      content_alignment: text-align-left
  __file__:
    key: __file__
    id: __file__
    input: markdown
    label: File
    accessorKey: __file__
    isMetadata: true
    skipPersist: false
    isDragDisabled: false
    csvCandidate: true
    position: 0
    isHidden: true
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: true
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Name:
    input: text
    accessorKey: Name
    key: Name
    id: Name
    label: Name
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: 1
    width: 344
    isSorted: true
    isSortedDesc: false
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      content_alignment: text-align-left
      wrap_content: true
  Type:
    input: tags
    accessorKey: Type
    key: Type
    id: Type
    label: Type
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Book", value: "Book", color: "hsl(250, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Status:
    input: select
    accessorKey: Status
    key: Status
    id: Status
    label: Status
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Not started", value: "Not started", color: "hsl(61, 95%, 90%)"}
      - { label: "In progress", value: "In progress", color: "hsl(41, 95%, 90%)"}
      - { label: "false", value: "false", color: "hsl(309, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Score:
    input: text
    accessorKey: Score
    key: Score
    id: Score
    label: Score
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    isSorted: false
    isSortedDesc: true
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Author:
    input: text
    accessorKey: Author
    key: Author
    id: Author
    label: Author
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 127
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      content_alignment: text-align-center
      wrap_content: true
  Completed:
    input: calendar
    accessorKey: Completed
    key: Completed
    id: Completed
    label: Completed
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Chapter:
    input: number
    accessorKey: Chapter
    key: Chapter
    id: Chapter
    label: Chapter
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Website:
    input: tags
    accessorKey: Website
    key: Website
    id: Website
    label: Website
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 168
    options:
      - { label: "Novelupdates", value: "Novelupdates", color: "hsl(187, 95%, 90%)"}
      - { label: "Scribblehub", value: "Scribblehub", color: "hsl(89, 95%, 90%)"}
      - { label: "RoyalRoad", value: "RoyalRoad", color: "hsl(32, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Link:
    input: select
    accessorKey: Link
    key: Link
    id: Link
    label: Link
    position: 100
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "https://www.novelupdates.com/series/after-taken-as-a-prisoner-of-war-the-vampire-queen-turned-me-into-a-vampire-and-made-me-her-daughter/", value: "https://www.novelupdates.com/series/after-taken-as-a-prisoner-of-war-the-vampire-queen-turned-me-into-a-vampire-and-made-me-her-daughter/", color: "hsl(168, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/212325/you-are-me/", value: "https://www.scribblehub.com/series/212325/you-are-me/", color: "hsl(53, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/117918/witches-of-welland/", value: "https://www.scribblehub.com/series/117918/witches-of-welland/", color: "hsl(86, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/181195/wish-of-the-cipher/", value: "https://www.scribblehub.com/series/181195/wish-of-the-cipher/", color: "hsl(142, 95%, 90%)"}
      - { label: "https://www.novelupdates.com/series/vicious-female-married-me-with-a-smile/", value: "https://www.novelupdates.com/series/vicious-female-married-me-with-a-smile/", color: "hsl(268, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/160509/velvet-abyss/", value: "https://www.scribblehub.com/series/160509/velvet-abyss/", color: "hsl(284, 95%, 90%)"}
      - { label: "https://www.novelupdates.com/series/two-as-one-princesses/", value: "https://www.novelupdates.com/series/two-as-one-princesses/", color: "hsl(177, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/158607/transfusion/", value: "https://www.scribblehub.com/series/158607/transfusion/", color: "hsl(275, 95%, 90%)"}
      - { label: "https://www.royalroad.com/fiction/35132/the-vampires-templar", value: "https://www.royalroad.com/fiction/35132/the-vampires-templar", color: "hsl(324, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/292180/the-time-i-got-reincarnated-as-a-seraph/", value: "https://www.scribblehub.com/series/292180/the-time-i-got-reincarnated-as-a-seraph/", color: "hsl(274, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/163923/the-sword-saints-second-life-as-a-fox-girl/", value: "https://www.scribblehub.com/series/163923/the-sword-saints-second-life-as-a-fox-girl/", color: "hsl(128, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/26125/the-reincarnated-master-craftsman-just-wants-to-live-a-peaceful-life/", value: "https://www.scribblehub.com/series/26125/the-reincarnated-master-craftsman-just-wants-to-live-a-peaceful-life/", color: "hsl(358, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/21898/the-other-world-is-leaking/", value: "https://www.scribblehub.com/series/21898/the-other-world-is-leaking/", color: "hsl(97, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/71729/the-demon-princess-high-school-life/", value: "https://www.scribblehub.com/series/71729/the-demon-princess-high-school-life/", color: "hsl(127, 95%, 90%)"}
      - { label: "https://www.novelupdates.com/series/the-creator-god-was-enslaved-by-her-yandere-sister/", value: "https://www.novelupdates.com/series/the-creator-god-was-enslaved-by-her-yandere-sister/", color: "hsl(289, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/297743/swarming-sovereignty/", value: "https://www.scribblehub.com/series/297743/swarming-sovereignty/", color: "hsl(314, 95%, 90%)"}
      - { label: "https://www.novelupdates.com/series/starchild-escapes-arranged-marriage/", value: "https://www.novelupdates.com/series/starchild-escapes-arranged-marriage/", color: "hsl(304, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/632699/soul-venerable/", value: "https://www.scribblehub.com/series/632699/soul-venerable/", color: "hsl(138, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/146137/soulseeker-online/", value: "https://www.scribblehub.com/series/146137/soulseeker-online/", color: "hsl(263, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/16995/second-life-as-the-sister-of-a-goddess/", value: "https://www.scribblehub.com/series/16995/second-life-as-the-sister-of-a-goddess/", color: "hsl(47, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/293353/reincarnation-as-a-fox-princess/", value: "https://www.scribblehub.com/series/293353/reincarnation-as-a-fox-princess/", color: "hsl(318, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/247555/reincarnated-as-a-sheep--path-to-becoming-the-strongest-demon-lord/", value: "https://www.scribblehub.com/series/247555/reincarnated-as-a-sheep--path-to-becoming-the-strongest-demon-lord/", color: "hsl(106, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/93502/reincarnated-as-an-op-loli/", value: "https://www.scribblehub.com/series/93502/reincarnated-as-an-op-loli/", color: "hsl(32, 95%, 90%)"}
      - { label: "https://www.novelupdates.com/series/reborn-as-the-heros-daughter-time-to-become-the-hero-once-more-wn/", value: "https://www.novelupdates.com/series/reborn-as-the-heros-daughter-time-to-become-the-hero-once-more-wn/", color: "hsl(41, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/310228/performative-masculinity/", value: "https://www.scribblehub.com/series/310228/performative-masculinity/", color: "hsl(65, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/242482/once-more-to-see-you/", value: "https://www.scribblehub.com/series/242482/once-more-to-see-you/", color: "hsl(174, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/292757/magical-girl-akis-secret/", value: "https://www.scribblehub.com/series/292757/magical-girl-akis-secret/", color: "hsl(192, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/144800/journey-to-amoraketh/", value: "https://www.scribblehub.com/series/144800/journey-to-amoraketh/", color: "hsl(161, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/67872/i-reincarnated-as-a-little-girl/", value: "https://www.scribblehub.com/series/67872/i-reincarnated-as-a-little-girl/", color: "hsl(34, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/131573/im-the-princess-of-the-ice-queen/", value: "https://www.scribblehub.com/series/131573/im-the-princess-of-the-ice-queen/", color: "hsl(268, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/263522/a-probability-experiment-turned-me-into-a-clockwork-girl-and-i-really-dont-know-what-to-make-of-it-all/", value: "https://www.scribblehub.com/series/263522/a-probability-experiment-turned-me-into-a-clockwork-girl-and-i-really-dont-know-what-to-make-of-it-all/", color: "hsl(290, 95%, 90%)"}
      - { label: "https://www.royalroad.com/fiction/49849/a-reincarnated-demons-life-of-wonder", value: "https://www.royalroad.com/fiction/49849/a-reincarnated-demons-life-of-wonder", color: "hsl(111, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/24213/black-witch-from-another-world/", value: "https://www.scribblehub.com/series/24213/black-witch-from-another-world/", color: "hsl(10, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/276881/boosted-restart--a-new-chance-in-a-different-world/", value: "https://www.scribblehub.com/series/276881/boosted-restart--a-new-chance-in-a-different-world/", color: "hsl(320, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/13113/bullied-/", value: "https://www.scribblehub.com/series/13113/bullied-/", color: "hsl(167, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/255452/caring-mother-hiatus/", value: "https://www.scribblehub.com/series/255452/caring-mother-hiatus/", color: "hsl(13, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/295604/cats-out-of-the-bag/", value: "https://www.scribblehub.com/series/295604/cats-out-of-the-bag/", color: "hsl(82, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/253998/faraway-survivor/", value: "https://www.scribblehub.com/series/253998/faraway-survivor/", color: "hsl(258, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/191085/gauntlette/", value: "https://www.scribblehub.com/series/191085/gauntlette/", color: "hsl(281, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/273707/happy-life-with-my-wife-hiatus/", value: "https://www.scribblehub.com/series/273707/happy-life-with-my-wife-hiatus/", color: "hsl(39, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/94389/hells-belles/", value: "https://www.scribblehub.com/series/94389/hells-belles/", color: "hsl(56, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/94162/i-am-succubus/", value: "https://www.scribblehub.com/series/94162/i-am-succubus/", color: "hsl(94, 95%, 90%)"}
      - { label: "https://www.novelupdates.com/series/i-became-a-beautiful-girl-but-im-still-an-mmo-junkie/", value: "https://www.novelupdates.com/series/i-became-a-beautiful-girl-but-im-still-an-mmo-junkie/", color: "hsl(28, 95%, 90%)"}
      - { label: "https://www.scribblehub.com/series/180043/im-in-a-monster-girl-world-mgw/", value: "https://www.scribblehub.com/series/180043/im-in-a-monster-girl-world-mgw/", color: "hsl(278, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
      option_source: manual
      wrap_content: false
config:
  remove_field_when_delete_column: false
  cell_size: normal
  sticky_first_column: true
  group_folder_column: 
  remove_empty_folders: false
  automatically_group_files: false
  hoist_files_with_empty_attributes: true
  show_metadata_created: false
  show_metadata_modified: false
  show_metadata_tasks: false
  show_metadata_inlinks: false
  show_metadata_outlinks: false
  show_metadata_tags: false
  source_data: current_folder
  source_form_result: 
  source_destination_path: /
  row_templates_folder: /
  current_row_template: 
  pagination_size: 200
  font_size: 16
  enable_js_formulas: false
  formula_folder_path: /
  inline_default: false
  inline_new_position: last_field
  date_format: yyyy-MM-dd
  datetime_format: "yyyy-MM-dd HH:mm:ss"
  metadata_date_format: "yyyy-MM-dd HH:mm:ss"
  enable_footer: false
  implementation: default
filters:
  enabled: false
  conditions:
```