# libcal-dept-names

Lists of SMU schools, centres and departments in JSON. They feed the **Remote data source Drop-down** field in LibCal registration forms, so every form draws from one shared list.

## Lists

| File | Contents | Catch-all option? |
|------|----------|-------------------|
| `smu-school-centers.json` | Schools, colleges, institutes and centres | No |
| `smu-all-depts.json` *(planned)* | The above + administrative departments | No |
| `public-all-depts.json` *(planned)* | Same as the matching list + `Not affiliated with SMU` and `Others` | Yes |

Use a `public-` list for forms open to non-SMU registrants. Use the plain list for SMU-only forms.

## Use in LibCal

1. In the LibCal form builder, add a **Dropdown (Remote Source)** field.
2. Paste the raw URL of the list you need, e.g.

   ```
   https://raw.githubusercontent.com/smu-libraries/libcal-dept-names/main/smu-school-centers.json
   ```

3. Save and preview the form to check that the options load.

## Updating a list

- Keep each file a plain JSON array of strings: `["Name A", "Name B"]`.
- **Use official names**. Each string is exactly what shows in the dropdown and in the registration data.
- **Order:** schools and colleges first, then institutes and centres, each group A–Z. Catch-all options always go last.
- Don't rename or move a file once forms use it; the URL is the link to LibCal.
- Renaming an entry doesn't change or update past registrations.


