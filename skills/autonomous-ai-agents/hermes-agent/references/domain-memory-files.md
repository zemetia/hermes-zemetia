# Domain-specific memory files

Use this pattern when a user wants durable, detailed memory for a specific area (businesses, projects, family context, research interests, etc.) but the built-in USER.md/profile memory should stay compact.

## Pattern

1. Keep USER.md concise: identity, stable preferences, and a short pointer to the domain file.
2. Create a separate markdown file under `/opt/data/memories/`, named for the domain in uppercase when user-facing, e.g.:
   - `/opt/data/memories/BUSINESS.md`
   - `/opt/data/memories/PROJECTS.md`
   - `/opt/data/memories/FAMILY.md`
3. Move detailed lists, project inventories, business descriptions, and long-form context into that domain file.
4. Patch `/opt/data/memories/USER.md` to link to the domain file instead of duplicating the long details.
5. Verify by reading both files back after writing/patching.

## Suggested structure

```md
# BUSINESS.md — Memori Bisnis <User>

File ini menyimpan konteks bisnis/proyek <User> secara lebih detail daripada USER.md.

## Konteks Besar
- ...

## Bisnis / Proyek Aktif
### 1. <Name>
- Jenis:
- Website:
- Status:
- Peran strategis:

## Pipeline / Akan Datang
- ...

## Cara Menggunakan Memori Ini
- Saat membantu dengan strategi, planning, branding, konten, growth, monetisasi, atau prioritas kerja, gunakan file ini sebagai konteks utama.
- Jangan menganggap semua item punya prioritas sama; tanyakan atau infer dari konteks mana yang sedang dibahas.
```

## Pitfalls

- Do not pack every detail into persistent memory entries when the content is too long; memory limits are tight and should hold compact facts.
- Do not remove the high-level pointer from USER.md; future sessions need a discoverable route to the domain file.
- Avoid stale operational logs, completed task histories, PR numbers, issue numbers, and other artifacts that will age out quickly.
