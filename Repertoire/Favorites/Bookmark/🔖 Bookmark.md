---

database-plugin: basic

---

```yaml:dbfolder
name: Bookmark Database
description: List of articles that might be relevant in the future.
columns:
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
    isHidden: true
    position: 2
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
  Topic:
    input: text
    accessorKey: Topic
    key: Topic
    id: Topic
    label: Topic
    position: 1
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 326
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Category:
    input: tags
    accessorKey: Category
    key: Category
    id: Category
    label: Category
    position: 3
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "ChatGPT", value: "ChatGPT", color: "hsl(175, 95%, 90%)"}
      - { label: "Github", value: "Github", color: "hsl(221, 95%, 90%)"}
      - { label: "Politics", value: "Politics", color: "hsl(216, 95%, 90%)"}
      - { label: "SteamDeck", value: "SteamDeck", color: "hsl(166, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Subcategory:
    input: tags
    accessorKey: Subcategory
    key: Subcategory
    id: Subcategory
    label: Subcategory
    position: 4
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Troll", value: "Troll", color: "hsl(279, 95%, 90%)"}
      - { label: "Github Access", value: "Github Access", color: "hsl(86, 95%, 90%)"}
      - { label: "Trump", value: "Trump", color: "hsl(62, 95%, 90%)"}
      - { label: "PS4 Emulation", value: "PS4 Emulation", color: "hsl(165, 95%, 90%)"}
      - { label: "WitchesVsPatriarchy", value: "WitchesVsPatriarchy", color: "hsl(351, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
  Text:
    input: text
    accessorKey: Text
    key: Text
    id: Text
    label: Text
    position: 6
    skipPersist: false
    isHidden: false
    sortIndex: -1
    width: 393
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
    position: 5
    skipPersist: false
    isHidden: false
    sortIndex: -1
    options:
      - { label: "Stackoverflow", value: "Stackoverflow", color: "hsl(198, 95%, 90%)"}
      - { label: "Reddit", value: "Reddit", color: "hsl(241, 95%, 90%)"}
      - { label: "[,Stackoverflow]", value: "[,Stackoverflow]", color: "hsl(343, 95%, 90%)"}
      - { label: "[,Reddit]", value: "[,Reddit]", color: "hsl(17, 95%, 90%)"}
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
      - { label: "https://stackoverflow.com/questions/68779331/use-token-to-push-some-code-to-github-support-for-password-authentication-was", value: "https://stackoverflow.com/questions/68779331/use-token-to-push-some-code-to-github-support-for-password-authentication-was", color: "hsl(258, 95%, 90%)"}
      - { label: "https://www.reddit.com/r/WhitePeopleTwitter/comments/148f1gl/trump_claims_that_while_president_he_pleaded_with/", value: "https://www.reddit.com/r/WhitePeopleTwitter/comments/148f1gl/trump_claims_that_while_president_he_pleaded_with/", color: "hsl(57, 95%, 90%)"}
      - { label: "https://www.reddit.com/r/ChatGPT/comments/14iw3sd/my_first_stab_at_a_potential_antitrolling_prompt/", value: "https://www.reddit.com/r/ChatGPT/comments/14iw3sd/my_first_stab_at_a_potential_antitrolling_prompt/", color: "hsl(158, 95%, 90%)"}
      - { label: "https://www.reddit.com/r/SteamDeck/comments/11pc06b/comment/jbycoxo/?context=3", value: "https://www.reddit.com/r/SteamDeck/comments/11pc06b/comment/jbycoxo/?context=3", color: "hsl(252, 95%, 90%)"}
      - { label: "https://www.reddit.com/r/WitchesVsPatriarchy/comments/177sf4u/comment/k4wdajj/?utm_source=share&utm_medium=web2x&context=3", value: "https://www.reddit.com/r/WitchesVsPatriarchy/comments/177sf4u/comment/k4wdajj/?utm_source=share&utm_medium=web2x&context=3", color: "hsl(16, 95%, 90%)"}
    config:
      enable_media_view: true
      link_alias_enabled: true
      media_width: 100
      media_height: 100
      isInline: false
      task_hide_completed: true
      footer_type: none
      persist_changes: false
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
  pagination_size: 10
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