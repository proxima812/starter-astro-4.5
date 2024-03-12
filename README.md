# astro starter 4.5 minimal

*стартер буду дорабатывать по мере понимая, чего нужно или чего убрать.*

## Необходимые настройки

- в settings.ts

## Для создания иконок из 1024x1024 используй сервис

- [favycon.vercel.app](https://favycon.vercel.app/)

## Пакеты

- astro 4.5
- tailwind
- sitemap
- rss
- astro-compress
- PWA

## Content Collection

Если **draft: true**, то НЕ будет в конечном итоге в сборке.

```ts
const items = defineCollection({
	schema: ({ image }) => {
		z.object({
			title: z.string().default("title"),
			description: z.string().default("description"),
			ogImage: image().optional(),
			// "2024-02-21T15:30:00Z"
			datePublished: z.union([z.string().datetime(), z.date()]),
			draft: z.boolean().default(false),
		})
	},
})
```

**/content/items/item.md**

## В папках

```md
├── astro.config.mjs
├── package-lock.json
├── package.json
├── public
│ ├── favicon.svg
│ └── favicons
│ └── icons
├── src
│ ├── assets
│ ├── components
│ │ ├── Favicons.astro
│ │ ├── SEOHead.astro
│ │ └── partials
│ │ ├── Footer.astro
│ │ └── Header.astro
│ ├── content
│ │ ├── config.ts
│ │ └── items
│ │ └── item.md
│ ├── data
│ ├── env.d.ts
│ ├── layouts
│ │ └── MainLayout.astro
│ ├── pages
│ │ ├── index.astro
│ │ ├── robots.txt.ts
│ │ └── rss.xml.js
│ ├── settings.ts
│ ├── styles
│ │ └── tailwind.css
│ └── utils
│ ├── libs
│ └── manifest.ts
├── tailwind.config.mjs
└── tsconfig.json
```
# starter-astro-4.5
