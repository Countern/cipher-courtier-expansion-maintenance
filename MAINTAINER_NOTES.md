# Maintainer's Notes

1. `/common/job_actions/landless_job_actions.txt`
   I do not know where the "aspiring_business_owner" modifier comes from, so
   I'm just gonna leave it there for now...
   But I did change the old character modifier condition to the new one.
2. This mod's `start_cadet_branch` decision overlapping with CK2Plus' `start_cadet_branch` decision
3. Localisation files to take note of:
   * `lalad_loc.csv` - **EVTDESChomeless_event.1** - Weird "ou'"
   * `ciphers_courtier_loc.csv` - **EVTDESmoving_events.5** - Unknown character after "ruler"
   * `troubles_courtier_loc.csv` - **EVTDESCtroublesevents.3** - The [GetName] in [Liege.GetName] is only for titles, not characters
   * `N/A` - **EVTDESrecruit_event.8 .7 .6** - Localisation key does not key, key refers to recruiting army 250 edition
4. Decisions to take note of:
   * `00_LALAD_decisions.txt` - **quit_job** - Decision not removing job traits and character flags after quitting
   * `00_LALAD_decisions.txt` - **move_court_to** - Players being able to move to their own liege's court
      * Might add another decision to pay homage or swear an oath to player's current liege as a courtier
   * `Courtier_troubles_decisions.txt` - **solve_trouble** - Immediate_Revolt province modifier still active once a rebellion start
      * Might add an on_action instance to solve the problem above
5. Events to take note of:
   * `courtier_visit_liege_capitals_events.txt` - **liegecap_events.6** - Description text too long, might convert to long_character_event or narrative_event
   * `courtier_wars_events.txt` - **courtierwar_events.3** - No need for AI ruler to have an option that rewards the player martial courtier, just reference the player courtier themselves in an immediate block
6. Minor titles files to take note of:
   * `courtier_title.txt` - **title_courtier** - A lot of missing code for a minor title instance

## Notes on missing stuff that's part of the mod
* Something about "aspiring_business_owner" char modifier
   * Missing modifier
   * Only tied to action_manage_business instance in `/common/job_actions/`
* Something about "constructing_courtier" char/title flag
* Something about "mod_quarry_knowledge" char modifier
   * Missing modifier
   * Tied to quarry events