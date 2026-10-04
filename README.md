# Samhalls `.github`-repo

> [!WARNING]
> **Det här repot är publikt.** Allt du committar här syns för hela internet, inklusive historiken.
> Lägg aldrig in hemligheter, interna URL:er, systemnamn, personuppgifter eller interna rutiner.
> Är du osäker: lägg det i ett internt repo istället.

Det här är ett specialrepo. GitHub läser vissa sökvägar här och använder dem som gemensamma standardvärden för alla repon i [Samhall-AB](https://github.com/Samhall-AB).

## Varför är det publikt?

GitHub kräver det. Ett `.github`-repo som ska leverera gemensamma filer till organisationens repon kan inte vara privat eller internt. Det publika läget är priset för att slippa kopiera samma mallar till varje repo.

## Vad vi får ut av det

| Sökväg | Effekt |
| --- | --- |
| `.github/ISSUE_TEMPLATE/` | Issue-mallar för alla repon som saknar egna |
| `profile/README.md` | Organisationens publika profilsida på [github.com/Samhall-AB](https://github.com/Samhall-AB) |
| `CONTRIBUTING.md`, `SECURITY.md`, `SUPPORT.md`, `CODE_OF_CONDUCT.md` m.fl. | Standardfiler för alla repon som saknar egna (finns inte här än) |
| `.github/pull_request_template.md` | Standard-PR-mall (finns inte här än) |

## Så fungerar arvet

- **Fallback, ingen merge.** Har ett repo en egen fil av samma typ används den. Org-filen ignoreras helt.
- **Issue-mallar är allt eller inget.** Finns det *någon* fil i repots egen `.github/ISSUE_TEMPLATE/` används inga av mallarna härifrån.
- **Filerna kopieras inte.** De följer inte med vid kloning eller nedladdning av enskilda repon.

## Vad som *inte* ärvs

`CODEOWNERS`, `dependabot.yml`, `LICENSE`, labels och workflows. Workflows här körs inte i andra repon. Centrala krav på workflows hanteras med rulesets.

Workflow templates kan ligga i ett `.github`-repo men behöver inte vara publika längre. Vill vi dela interna mallar gör vi det på annat sätt än här.

## Bidra

1. Gör ändringar via PR, aldrig direkt mot `main`.
2. Läs igenom diffen med publik-glasögonen på: skulle det här vara okej på en skylt utanför kontoret?
3. Kom ihåg att ändringar slår igenom direkt i alla repon som saknar egna filer.

## Läs mer

- [Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [Customizing your organization's profile](https://docs.github.com/en/organizations/collaborating-with-groups-in-organizations/customizing-your-organizations-profile)
