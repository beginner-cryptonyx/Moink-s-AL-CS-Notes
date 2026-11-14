---
subject:
  - "[[Computer Science]]"
grade:
  - "[[AS Level]]"
related: 
creation-date: 2024-12-02
up:
  - "[[SQL]]"
  - "[[Database (CS)|database]]"
  - "[[03. Efforts/Ongoing/Programming]]"
---
```SQLite
ALTER TABLE <table_name>
	ADD FOREIGN KEY (<field_name>)
	REFERENCES <main_table_name>(<primary_key_of_main_table>)
```