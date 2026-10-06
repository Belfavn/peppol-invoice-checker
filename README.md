# Peppol Invoice Checker

A Claude plugin that validates, explains and drafts Belgian Peppol e-invoices
(UBL, Peppol BIS Billing 3.0), and checks EU VAT numbers, in English, French
or Dutch.

> **Status: in development.** The tools are not live yet. Do not install.

## What it does

| Tool | What you get |
| --- | --- |
| `validate_invoice` | Every error and warning in an invoice XML, explained in plain language with a suggested fix |
| `explain_invoice` | A readable summary of an XML invoice: parties, lines, VAT, totals; optional CSV |
| `check_vat_number` | The registered name and address for an EU VAT number, from the EU VIES service |
| `draft_invoice` | A new UBL invoice from your details or an existing PDF, validated before it is returned |
| `save_to_document_desk` | Keeps a validated invoice in Belfavn Business Desk |

Validation, explanation and VAT checks are free up to a monthly limit with a
free Belfavn account. Drafting and saving are part of the Business Desk plans.

## How it works

The plugin connects Claude to a remote MCP server operated by Belfavn
(`.mcp.json`) and adds a skill (`skills/peppol-invoices/`) that tells Claude
when to use each tool and how to explain results. You sign in with a Belfavn
account the first time a tool is used.

## Privacy

Invoices are processed to answer your request and are not stored unless you
ask to save one. Usage is counted per account for plan limits; invoice content
is not logged.

## Not advice

This plugin checks invoices against published Peppol rules. It is not tax,
accounting or legal advice, and a passed check does not guarantee that an
invoice is legally compliant.

## Support

Belfavn — https://belfavn.com

## Licence

MIT. See [LICENSE](LICENSE).
