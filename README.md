# Sales Insights Gauges for Dynamics 365

A set of three lightweight web resource widgets designed to surface Sales Insights data directly on the Opportunity form in Microsoft Dynamics 365.

## Widgets

### Opportunity Score (`opportunity-score.html`)
Displays the AI-powered predictive opportunity score as a circular gauge (0–100), with grade label, trend direction, and positive/negative scoring factors.

### Relationship Health (`relationship-health.html`)
Shows the relationship health status (Good / Fair / Poor) with a horizontal gauge bar, trend indicator, next and last interactions, and activity summary stats (emails, meetings, calls, tasks).

### Assistant (`assistant.html`)
Renders action card notifications from the Sales Assistant — expandable cards with type icons, titles, and descriptions. Supports 20+ card types including meeting reminders, email follow-ups, opportunity closing alerts, and competitor mentions.

## Data Sources

| Widget | Entity | Key Fields |
|--------|--------|------------|
| Opportunity Score | `msdyn_predictivescores` | score, grade, trend, score reasons |
| Relationship Health | `msdyn_opportunitykpiitems`, `activitypointers` | health state, health value, trend, activities |
| Assistant | `actioncards` | card type, title, description |

## How to Use

1. **Upload each HTML file as a Web Resource** in your Dynamics 365 environment.
2. **Add to the Opportunity Form** — place each widget in the desired section of the Opportunity main form.
3. **Publish** — save and publish the form.

## Requirements

- Microsoft Dynamics 365 Sales (online)
- **Sales Insights** must be enabled for predictive scoring and relationship health data
- Action cards must be active for the Assistant widget

## License

[MIT](LICENSE.txt)
