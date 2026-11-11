# Assembly Connect — initial wireframes

Working title for a civic reporting tool serving one Ghanaian Metropolitan, Municipal or District Assembly. The municipality, agency contacts and partnership are not yet selected. All examples and counts in these wireframes are fictional.

Open [the gallery](index.html) in a browser, or open the SVG/PNG files directly. The gallery links between boards; depicted app controls are sketches, not working forms.

## User flows

1. **Discover:** Search or browse the map/list, filter reports by category and status, and select a report.
2. **Contribute to an existing report:** Select “This affects me too,” add an observation/photo, or follow updates. Supporting an issue is distinct from confirming its existence. A signed-in participant can support a report once and withdraw that support.
3. **Create a report:** Choose a category; use device location with permission or enter a location manually; correct the pin; optionally take/upload a photo. Check nearby reports before continuing. Complete description, observed date and category-specific impact questions.
4. **Review and submit:** Check the details, then save. Show confirmation only after the database succeeds. A saved report is not evidence of agency receipt. Retain the draft and offer Retry if submission fails.
5. **Follow progress:** See dated observations and official responses, follow updates, and provide evidence if a problem changes or remains unresolved. Residents request another review rather than directly editing official status.
6. **Assembly review:** Authorized staff inspect the queue, correct routing, set priority, provide a reason, publish an update, or refer a report. Record the previous and new status with reviewer and date. An official response must come from an authorized reviewer; demo actions must be labeled as such.

## Boards

| Board | Contents |
| --- | --- |
| [01 — Resident map](01-resident-map.svg) | Desktop browsing, filters, status legend and selected issue details |
| [02 — Mobile reporting](02-mobile-report.svg) | Location, optional photo, duplicate suggestion and impact questions |
| [03 — Submission and follow-up](03-submission-follow-up.svg) | Review, confirmation, report reference, timeline and observations |
| [04 — Assembly review](04-assembly-review.svg) | Queue, evidence, assignment, priority, status and official updates |

## Status, impact and priority

- **Status:** Submitted → Acknowledged → In progress → Resolved. Referred is an alternative where another body is responsible. A referral does not establish acceptance by that body.
- **Reported impact:** Observable category-specific answers, with an “I’m not sure” option. For a blocked drain: blocked without observed flooding; overflow on road/footpath; water entering a property; uncertain.
- **Community support:** Number of participants selecting “This affects me too”; not a severity score or representative population estimate.
- **Assembly priority:** Initially awaiting assessment. Authorized staff select High, Normal or Low using criteria agreed with the assembly. Support counts do not automatically rank repairs.
- **Map encoding:** Grayscale wireframes show structure. Final marker status needs readable labels and distinguishable symbols as well as color; impact and priority appear separately in details.

## Implementation scope and accessibility

Start with one municipality, three agreed report categories and the shared map/report/review loop. Account access is needed for reviewer permissions and controlled support actions. Exact sign-in and subscription methods remain implementation decisions. There is no AI dependency.

On mobile, browsing defaults to an accessible report list with a Map toggle; selected report details open as a full-width panel. The reporting boards show a stacked mobile form. The desktop reviewer queue can become stacked cards on narrow screens.

Every map action needs a list, search or form alternative. Use labeled inputs, visible focus, adequate touch targets, keyboard-operable dialogs, and inline error messages. Announce successful submissions and errors. Do not require a photo or location permission to report. Public content includes the issue location, photo and description; contact details remain private. Actual upload privacy handling and storage access rules must be implemented before collecting real reports.

The prototype does not send reports to a government body. Provide an honest notice until a receiving channel and agency relationship exist. Any urgent-danger guidance must point to verified local channels rather than promise immediate handling through this app.

## Copy into the class pull-request description

These images document the proposed participation workflow, not a finished implementation. GitHub-relative paths below refer to files on the PR's head branch; if they do not render in the class repository, upload the PNGs to the PR description or use raw URLs from your own repository.

```markdown
### Initial wireframes — Assembly Connect

Residents can report local issues with photos and map locations, support existing reports, and follow dated updates. Assembly reviewers can assign teams, assess priority and publish progress. The pilot municipality is still to be selected.

![Resident map and issue details](docs/wireframes/01-resident-map.png)
![Mobile reporting flow](docs/wireframes/02-mobile-report.png)
![Review, submission and follow-up](docs/wireframes/03-submission-follow-up.png)
![Assembly review workspace](docs/wireframes/04-assembly-review.png)
```

## Design references

- [Course engagement instructions](../../INSTRUCTIONS.md): contributions to a shared spatial dataset, persistence, mobile use and accessibility.
- [FixMyStreet routing](https://fixmystreet.org/how-it-works/): use category and location to identify the responsible body.
- [SeeClickFix priority controls](https://www.civicplus.help/seeclickfix/docs/prioritize-a-request): staff priority is distinct from community participation.
- [Oxfordshire assessment process](https://www.oxfordshire.gov.uk/transport-and-travel/transport-policies-and-plans/highway-maintenance/26-highway-transparency-report): assess observed risk and context.

Prepared November 4, 2026.
