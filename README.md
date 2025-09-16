# Personal Planner

A GitHub-based personal planning system using Issues and markdown files for task management across multiple time horizons.

## Structure

```
planner/
├── daily/
│   └── YYYY/
│       └── MM-month/
│           └── YYYY-MM-DD.md
├── weekly/
│   └── YYYY/
│       └── week-NN.md
├── monthly/
│   └── YYYY/
│       └── YYYY-MM-month.md
├── quarterly/
│   └── YYYY/
│       └── YYYY-qN.md
├── annual/
│   └── YYYY-goals.md
│   └── YYYY-review.md
├── templates/
│   ├── daily.md
│   ├── weekly.md
│   ├── monthly.md
│   ├── quarterly.md
│   └── annual.md
└── projects/
    └── project-name/
        └── README.md
```

### File Types

- **Daily**: `daily/YYYY/MM-month/YYYY-MM-DD.md` - Daily tasks and reflection
- **Weekly**: `weekly/YYYY/week-NN.md` - Weekly summaries and planning
- **Monthly**: `monthly/YYYY/YYYY-MM-month.md` - Monthly reviews and goals
- **Quarterly**: `quarterly/YYYY/YYYY-qN.md` - Quarterly roadmaps
- **Annual**: `annual/YYYY-goals.md|review.md` - Annual planning and reviews
- **Templates**: Standard markdown templates for consistent planning
- **Projects**: Long-term project documentation and tracking

## Usage

- **GitHub Issues**: Track tasks spanning 2+ days with priority and category labels
- **Projects**: Organize related issues using Kanban/Table/Timeline views
- **Templates**: Standard markdown templates for consistent planning
- **Cross-reference**: Link between markdown files and GitHub issues

See [CLAUDE.md](CLAUDE.md) for detailed system documentation and workflows.