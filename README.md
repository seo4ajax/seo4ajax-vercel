# Integration in the `vercel.json` file

SEO4Ajax can be integrated on vercel by adding a new rule in the `"rewrites"` property of the `vercel.json` file. You just have to replace `<token>` with your site token on SEO4Ajax.

```json
{
  "rewrites": [
    {
      "source": "/:path(.*)",
      "has": [
        {
          "type": "header",
          "key": "user-agent",
          "value": ".*google|bot|lighthouse|spider|pinterest|crawler|archiver|flipboardproxy|mediapartners|facebookexternalhit|insights|quora|whatsapp|slurp.*"
        }
      ],
      "destination": "https://api.seo4ajax.com/<token>/:path*"
    }
  ]
}
```

Warning: This configuration works for all application paths except the home page.
