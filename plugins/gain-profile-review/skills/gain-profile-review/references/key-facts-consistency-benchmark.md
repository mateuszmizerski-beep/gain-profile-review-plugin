# Gain.pro Poland Full Profiles: Key Facts and General Consistency Benchmark

Version: 2026-06-13

## Navigation

- Sections 1-3: customers, channels/activities, and headquarters.
- Sections 4-6: FTEs, ownership/deal dates, and founding year.
- Sections 7-8: aliases, tags, short activity, and writing consistency.
- Sections 9-10: operational procedure and expert-calibration questions.

## Purpose and scope

This benchmark reapplies the Gain Key Facts and General Consistency guidance to the same 232 Polish Full profiles used in the three earlier practical-review rounds. Each profile was refreshed from Gain with the Business, ownership, FTE, and deals packages.

The purpose is not to certify published profiles as correct. Live profiles are useful evidence of platform conventions, but they also contain omissions and inconsistencies that a reviewer should catch. The written Gain guidance remains authoritative when practice and theory conflict.

The connector exposed the following fields sufficiently for review: aliases, short business-activity comment, sector and subsector, tags, Business text, headquarters city/country/address, founding year, structured activities, customer base, sales channels, price positioning when populated, latest FTE and year, ownership type/history/investors, and last deal month/year.

The connector did not expose secondary URLs, parent links, every CMS investor flag, or the underlying financial workbook. Findings involving those fields therefore remain outside this measured audit. Exact FTE consistency with financials could not be tested; Business-to-Key-Facts consistency could.

## Coverage snapshot

| Field | Observable result |
|---|---:|
| Full profiles reviewed | 232 |
| Customer-base field populated | 232 |
| Business-activity field populated | 232 |
| Sales-channel field populated | 228 |
| Headquarters address populated | 230 |
| Structured FTE figure populated | 231 |
| Price positioning visibly populated | 1 |

Price positioning should not be inferred to be non-compliant merely because it was usually absent: the field is optional and the connector may omit a `Not applicable` value.

## 1. Customer-base consistency

### Explicit contradictions

Six profiles explicitly state a material customer type in the Further information paragraph but do not select the corresponding Key Facts field:

| Profile | Business says | Key Facts omits |
|---|---|---|
| Animex Foods | B2B and B2C | B2C |
| Lancerto | B2C and, to a lesser extent, B2B | B2B |
| Komputronik | B2C, B2B and B2G | B2G |
| PESA Bydgoszcz | B2B and B2G | B2G |
| GTC | B2B and B2C | B2C |
| Selvita | B2B and, to a lesser extent, B2G | B2G |

These are review findings, not harmless stylistic differences. The reviewer should determine whether the prose overstates an immaterial segment or the Key Facts tick is missing, then correct both representations together.

Erbud shows the reverse type of problem: Business says `B2G and B2G`, while Key Facts selects B2B and B2G. The likely intended prose is B2B and B2G, but this must be corrected through factual verification rather than silently assumed.

### B2B2C and B2G2C conflict

Published practice frequently uses B2B2C or B2G2C language and then selects both the direct payer and the end-user category. Examples include CD Projekt, Cersanit, Nowy Styl, People Can Fly, Hortex, Voxel, Zdrowit, and NU-MED.

This conflicts with the written direct-revenue rule, under which sales to retailers are normally B2B only and a reimbursed patient does not automatically make the public payer a direct customer category. Until expert clarification, the reviewer model should:

1. Identify the entity that pays the profiled company.
2. Apply the approximately 10% revenue-materiality threshold.
3. Treat B2B2C/B2G2C as descriptive route-to-end-user wording, not automatically as permission to tick both endpoints.
4. Flag published dual-tick precedent as a policy question rather than copying it blindly.

Natural-language customer descriptions can support a selected field even without an abbreviation. For example, InPost's reference to `individual customers` supports B2C. A review must therefore read meaning, not merely compare strings.

## 2. Sales channels and activities

### Missing sales-channel fields

Four profiles have no sales channel selected despite clear routes to market in Business:

- Animex Foods: sales through supermarkets, hypermarkets, convenience stores, and online retail indicate indirect sales, with online exposure where material.
- Euvic: Business explicitly mentions direct sales and an omnichannel distribution network for hardware.
- Molecure: licensing and collaboration agreements indicate a direct contractual route to pharmaceutical partners.
- GTC: rental agreements and asset disposals indicate direct sales/contracting.

This is a high-confidence completeness finding because at least one activity, customer type, and sales channel is expected.

### Practical activity patterns

The sample supports several useful, non-mandatory patterns:

- All 18 Software profiles select Services; 17 also select Engineering.
- Twenty-seven of 28 Food profiles select Manufacturing.
- All 18 Retail profiles select Retail.
- All 12 Technical services profiles select Services.
- All five Biotechnology profiles select R&D.
- Both Telecom profiles select Services and Operator.

These patterns are useful comparables, not automatic rules. The operating model still controls. OTCF is a good example of correctly omitting Manufacturing because production is explicitly outsourced. Euvic is a likely inconsistency in the other direction: it is described as an IT-services and hardware-distribution group, but selects Engineering, Manufacturing, and R&D while omitting Services and Distribution.

Do not infer an activity from an incidental word. A software company serving manufacturing clients is not a manufacturer; a company producing media content does not necessarily perform Manufacturing; and a retailer carrying third-party products does not perform Distribution merely because products are distributed to consumers.

## 3. Headquarters and address

Two profiles lack the structured city/address even though Business states a headquarters:

- Animex Foods: Warsaw (PL).
- Wittchen: Palmiry (PL).

Fourteen additional profiles have a city or country difference between Business and Key Facts. Some are obvious errors:

- Cersanit: Business says Kielce (UK); Key Facts correctly points to Kielce, Poland.
- Akomex: Business says `Starograd Gdański`; the address says `Starogard Gdański`.
- Booksy: Business says Chicago (US); Key Facts says Warsaw (PL).
- JSW: Business says Warsaw; Key Facts says Jastrzębie-Zdrój.
- Pelion: Business says Toruń; Key Facts says Łódź.
- Morele: Business says Kraków; Key Facts says Warsaw.

Other differences may reflect an operating headquarters, registered office, nearby municipality, or postal locality: Dega, Cedrob, Tarczyński, Apator, Mo-BRUK, R-GOL, Ecowipes, and Transsystem. They still require verification. The correct response is not to force text to the database mechanically, but to establish which location is the actual headquarters and then align the exact Key Facts address and Business city/country.

International English variants are not inconsistencies: Warsaw/Warszawa, Cracow/Kraków, and diacritic differences should be normalized before raising a finding.

## 4. FTE and employee consistency

A machine-assisted comparison was normalized for commas, `k` notation, approximate figures, decimal FTEs, and FY labels. It found:

| Comparison outcome | Profiles |
|---|---:|
| Same year and aligned within rounding tolerance | 138 |
| Same year but materially different value | 5 |
| Different year, same/compatible value | 27 |
| Different year and different value | 60 |
| Business wording defective or missing | 1 |
| Missing in both Business and Key Facts | 1 |

The five same-year material discrepancies are especially strong review findings:

- Allegro: 6,090 employees in Business versus 5,754 FTEs in Key Facts for 2025.
- MODIVO: 15,704 employees versus 17,528 FTEs for 2025.
- Huuuge Games: 328 employees versus 301 FTEs for 2025.
- Euvic: approximately 6,500 group employees versus 634 FTEs for 2025.
- Grupa Tauron: approximately 25,000 employees versus 19,096 FTEs for 2025.

Euvic is the clearest perimeter warning: the prose appears to describe the group, while the structured figure likely reflects a narrower legal entity or consolidation basis. Animex Foods is another severe perimeter candidate even though the dates differ: approximately 11,000 employees in Business versus 243 FTEs in Key Facts.

Different dates are also consistency findings under the written rule, even where both values may be individually defensible. They usually indicate that one field was refreshed without the other. The reviewer should establish one latest, like-for-like figure and align:

- group/legal-entity perimeter;
- employees versus FTEs convention;
- average versus period-end measurement;
- value and measurement date;
- Business, Key Facts, and financial workbook.

Do not treat a difference as solved merely because both figures fall in the same employee range.

Wosana contains a writing defect: `had 281 on average over FY2022` omits `employees` or `FTEs`. FixMap lacks both a Business headcount and a structured FTE; this is acceptable only if reasonable research confirms that no reliable figure is available.

## 5. Ownership and last deal date

The ownership distribution was 88 listed, 76 private, 35 PE-majority/controlled, 14 PE-minority, eight VC-backed, ten subsidiaries, and one other.

All 35 PE-majority and all 14 PE-minority profiles have a last deal date. Seven of eight VC-classified profiles have one. This supports the positive rule for investor-backed assets.

Eight profiles populate a date despite an ownership type for which the written guidance says it should be blank:

- Listed: Allegro, InPost, Selena Group, and Grupa PTWP.
- Private: Qemetica.
- Subsidiary: Shoper, Danwood, and R-GOL.

Some dates correspond to an IPO, delisting, minority transaction in a listed company, or an old acquisition. Those events may belong in Background or deals, but do not automatically belong in the Key Facts last-deal field.

Molecure is classified as VC-backed while Background describes a publicly listed company. Its empty last-deal date is less important than resolving the ownership classification itself: any publicly traded shares should normally result in Publicly listed.

## 6. Founding year and Background

The Key Facts founding year does not appear in six Backgrounds:

- Grupa Azoty: Key Facts 1927; Background says established in 1929.
- Rawlplug: Key Facts 1982; Background says founded in 1912.
- Koral: Key Facts 1978; Background says founded in 1979.
- WB Group: Key Facts 1997; Background says founded in 1998.
- LUG Group: Key Facts 1989; Background names the founders but omits the year.
- Euvic: Background is empty.

The first four require underlying-business and legal-history verification; they should not be resolved by choosing whichever date appears more often. LUG requires the year to be added if verified. Euvic requires a complete Background, including current ownership.

## 7. Aliases, short activity, sector, and tags

### Aliases

Five official names containing Polish characters lack the normalized search alias required by the guidance:

- Jastrzębska Spółka Węglowa -> `Jastrzebska Spolka Weglowa`.
- Instal Kraków -> `Instal Krakow`.
- Tarczyński -> `Tarczynski`.
- Ceramika Paradyż -> `Ceramika Paradyz`.
- Zakłady Przemysłu Cukierniczego Skawa -> `Zaklady Przemyslu Cukierniczego Skawa`.

Normalization should preserve the full official name. A short trading name such as `Skawa` does not replace the searchable ASCII form of the legal/official name.

### Short business-activity comment

All 232 profiles contain a short comment. The median is 30 characters and four words. Thirty comments exceed the approximate 35-character target, but the longest is only 45 characters. This strongly supports treating 35 characters as soft guidance: concise accuracy matters more than forced truncation.

The comments often use noun phrases such as `production of...`, `software development`, and `distribution`. Review against the rule that the field describes an activity rather than the asset, and prefer `and` over `&` when space permits.

### Subsector tags

Eighteen profiles do not include the selected subsector as a tag after normalizing standard mappings such as Food -> `food and beverage` and Professional services -> `professional services`. Examples include Animex Foods, Erbud, Empik, Euvic, Symfonia, ONDE, and FixMap.

Conversely, 49 profiles contain 75 tags that duplicate non-subsector structured business-model fields. The most common are Manufacturing (20 profiles), Distribution (15), Retail (15), Design (11), R&D (seven), Engineering (five), and Brick-and-mortar (two).

The review rule is asymmetric:

- The selected subsector must appear as a tag even though it overlaps the classification.
- Activity, channel, customer-base, and price-position fields should not be repeated as generic tags.
- A compound, economically meaningful search term is not automatically redundant merely because it contains a related word; judge the whole tag.

## 8. General writing consistency

The refresh found several simple defects that a final review should catch:

- Missing final full stop in Trans Polonia Group's At-a-glance, Displate's At-a-glance, and Vehis Group's customer paragraph.
- Decimal commas in Farmacol (`36,6`) and Grupa Tauron (`72,8`) within English prose.
- Akomex's `Starograd`/`Starogard` typo.
- Cersanit's Poland/UK country-code error.
- Erbud's duplicated `B2G and B2G` customer wording.
- Wosana's missing employee/FTE noun.
- Pelion's double space in `as of  FY2024`.

These examples reinforce a useful review order: first find factual contradictions and missing fields, then perimeter/date mismatches, then mechanical language defects. A polished sentence remains wrong if the structured profile tells a different story.

## 9. Operational review procedure learned from the sample

For every Full profile, the model should build a compact internal consistency table before commenting:

| Topic | Compare |
|---|---|
| Identity/perimeter | Official name, aliases, group composition, URL set, parent, ownership |
| Classification | Short activity, sector/subsector, activities, tags, Business |
| Customers | Further information, customer-base ticks, direct payer, materiality |
| Route to market | Revenue model, sales-channel ticks, owned versus third-party channel |
| Location | Actual HQ, exact address, Business city/country |
| People | Count, date, perimeter, employees/FTEs, average/period-end, financials |
| Ownership | Type, investors, parent, Background ending, current-investor flags |
| Deals | Latest qualifying investor deal, announcement date, ownership type |
| Origin | Founding year, underlying-business logic, Background |
| Positioning | Price field, Business/Market wording, Assessment |
| ESG | Badge, ESG prose, company-specific evidence, Assessment |

Classify findings as:

1. **Direct contradiction:** two fields cannot both be correct.
2. **Missing structured field:** prose clearly supports a required tick/value, but it is absent.
3. **Perimeter or convention mismatch:** both figures may be sourced but refer to different entities, dates, or measurement bases.
4. **Likely stale field:** one section has been refreshed and another has not.
5. **Verification candidate:** a difference may reflect a legitimate operating/registered-office or materiality distinction.
6. **Mechanical/style defect:** punctuation, spelling, capitalization, units, or platform notation.

Only the last category can normally be fixed without substantive research.

## 10. Questions for expert calibration

1. When Business uses B2B2C/B2G2C, should reviewers enforce the direct-revenue rule strictly and select only the payer, or select the end-user category as well when end demand is material? Live profiles frequently do the latter.
2. When structured FTEs come from a narrower legal entity but Business describes a consolidated group headcount, should the profile always replace the structured value with the group figure, or can the financial perimeter control if clearly labelled?
3. For headquarters, should Key Facts always contain the operating headquarters used in Business, even when the registered/legal address is elsewhere, or is there a preferred hierarchy of sources?
4. Is the prohibition on last deal dates for listed companies absolute even when a PE investor makes a disclosed minority investment in the listed asset, as in InPost or Grupa PTWP?

## Bottom line

The practical exercise strongly validates the Key Facts and General Consistency theory. The most important additional lesson is that review cannot be a checkbox comparison. The model must reason about payer versus end-user, group versus legal-entity perimeter, operating versus registered headquarters, investor versus strategic transactions, and the measurement convention behind every repeated number.

The 232 live profiles provide excellent tone and structure examples, but they also demonstrate why the model must treat cross-profile precedent as evidence, not permission to reproduce an inconsistency.
