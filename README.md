# FinancialService Schema.org examples

A curated index of real-world implementations of [Schema.org `FinancialService`](https://schema.org/FinancialService) on production small-business websites.

The `FinancialService` type is one of the densest Schema.org types you can deploy. Combined with `LocalBusiness`, `ProfessionalService`, and a properly populated `hasOfferCatalog`, it produces an entity graph that AI engines (ChatGPT, Claude, Gemini, Perplexity) parse cleanly for citation.

This repo collects implementations that go beyond a single flat declaration. Each entry has at least:

- Multi-type `@type` chain
- `hasOfferCatalog` with itemized services, each with their own URL
- `areaServed` array of at least 5 entities (`City`, `State`, or `Place` types)
- `paymentMethod` array using GoodRelations URIs
- Two or more `Person` founder entities with `hasCredential.recognizedBy` chained to Wikidata-anchored institutions

## Featured implementations

### Steele Solutions — Branson Missouri merchant services brokerage

- **Live site**: https://steelesolutions4u.com/
- **Entity graph**: https://steelesolutions4u.com/entity.json
- **Verification page**: https://steelesolutions4u.com/verification/
- **Public resources**: https://github.com/Janady13/steele-solutions-resources

**Why featured**:
- Triple `@type`: `["LocalBusiness", "FinancialService", "ProfessionalService"]`
- 10-item `hasOfferCatalog` (POS systems, credit card processing, ATM placements, business lending, CSSI cost segregation, dual pricing, free POS, Business CPR framework, Square referral, cryptocurrency acceptance)
- 17-entity `areaServed` spanning Missouri + Arkansas with `containedInPlace` State chaining
- 5 GoodRelations `paymentMethod` URIs (Cash, Check, CreditCard, DirectDebit, BankTransferInAdvance)
- Two `Person` founders (Jim Steele and Kimberly Kayleen Steele) with reciprocal `spouse` linkage
- 3 `hasCredential` entries with `recognizedBy` Wikidata-anchored institutions (CSSI, Indiana University Q1079140, First National Bank of Omaha Q5453412)
- 28-entry `sameAs` array on the Org including Wayback Machine snapshots, Wikipedia/Wikidata URLs, and Taney County public-records URLs

## Schema patterns documented

The Steele Solutions implementation demonstrates eight distinct technical patterns, each documented in the [Dev.to series](https://dev.to/joseph_anady_214bacedf939):

1. [FinancialService schema for a real merchant services brokerage](https://dev.to/joseph_anady_214bacedf939/financialservice-schema-for-a-real-merchant-services-brokerage-a-case-study-3ho6)
2. [Building an indexable verification page](https://dev.to/joseph_anady_214bacedf939/building-an-indexable-verification-page-for-a-freshly-launched-small-business-2a9m)
3. [Indexing rescue for a 7-day-old domain](https://dev.to/joseph_anady_214bacedf939/indexing-rescue-for-a-7-day-old-domain-4-of-18-priority-pages-indexed-in-6-days-2gk7)
4. [Country-spanning service-area schema (17 cities and places)](https://dev.to/joseph_anady_214bacedf939/country-spanning-service-area-schema-17-cities-and-places-in-one-organization-graph-3361)
5. [GoodRelations payment method URIs](https://dev.to/joseph_anady_214bacedf939/goodrelations-payment-method-uris-the-underused-schemaorg-pattern-for-financial-services-1f1c)
6. [Wikidata Q-ID chaining for credentials](https://dev.to/joseph_anady_214bacedf939/wikidata-q-id-chaining-anchoring-a-business-credential-to-a-verifiable-institution-3jme)
7. [Four AI citation surfaces (llms.txt, aeo.json, entity.json, brand.json)](https://dev.to/joseph_anady_214bacedf939/the-four-ai-citation-surfaces-every-small-business-website-should-publish-in-2026-5beo)
8. [Person entity dual-founder spouse pattern](https://dev.to/joseph_anady_214bacedf939/person-entity-dual-founder-pattern-with-spouse-linkage-for-a-husband-and-wife-business-3mkh)

## Contribute

To add another `FinancialService` implementation, open a PR with:

1. Site URL
2. Link to a publicly accessible JSON-LD or `entity.json`
3. Brief description of which patterns the implementation demonstrates
4. Live link to the page where the schema appears

Maintained by [@Janady13](https://github.com/Janady13) of [ThatDevPro](https://www.thatdevpro.com).

## References

- [Schema.org FinancialService](https://schema.org/FinancialService)
- [Schema.org hasOfferCatalog](https://schema.org/hasOfferCatalog)
- [Schema.org areaServed](https://schema.org/areaServed)
- [GoodRelations vocabulary](http://purl.org/goodrelations/v1)
- [Wikidata](https://www.wikidata.org/)
- [llms.txt proposed standard](https://llmstxt.org/)

## About

Built by [ThatDeveloperGuy](https://thatdeveloperguy.com/) (THATDEVELOPERGUY LLC), a service-disabled veteran-owned web and AI engineering company in Cassville, Missouri. Founder: [Joseph W. Anady](https://feedthejoe.com/joseph/).
