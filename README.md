# Claudiu Cristian Sandu

Senior full-stack engineer in Copenhagen. I have written TypeScript for ten years.

Most of my work sits in private company repositories. This page describes it, because
the code cannot.

## What I build

I started on the back end. Then came years of front-end work, and I closed the gap
between the two on purpose rather than by drift. So I have shipped both halves of a
product: the interface people use, and the system behind it. My depth is on the server
side, where correctness matters most.

My current work is payment reconciliation. A bank collects rent by direct debit
and an accounting ledger records it. The two must agree every day. When they disagree,
the work is finding out why.

Three things I am strongest at:

**Data integrity.** I write database migrations against live schemas. I keep money in
integer units, so rounding cannot lose it. And I put a rule in the database when the
application is the wrong place for it. One example: a building can hold two rent
regulations at the same time, but their date ranges must never overlap. That is a
constraint on the data. It belongs in a unique index, not in a method someone can
bypass.

**Silent failures.** I look for the errors that print no error. A function that skips a
record and reports success is worse than a crash, because nobody sees it. Most of the
defects I find are this shape.

**Tests that can fail.** A test that cannot fail is not a test. So I break the code on
purpose and check that the right test goes red, and only that one. If nothing goes red,
the test was decoration. Almost half the code I write is test code.

## Experience

**Senior Software Engineer — Felix Technologies** · 2025–present
Property management SaaS: tenancies, invoicing, deposits, and rent regulation.
I owned the payment reconciliation between the Danish direct-debit system and an
accounting platform. I took it from the first analysis through to production.
I learned the settlement file format from real files, not from the specification.
That changed what we chose to build.
Payment slips turned out to be a separate product from direct debit, rather than a flag
on one. It took a close read of the specification to see that. Until then we were
dropping the inbound confirmations, which meant money arrived and no invoice ever
recorded it. The awkward part was that the slip reference does not survive the round
trip, so there is nothing obvious to join on. I matched on what does come back — the
creditor, the customer number, the amount and the date. When two invoices fit equally
well, the system stops and asks a person rather than guessing.
`TypeScript · Node · TypeORM · GraphQL · PostgreSQL · AWS Lambda · SQS · react-admin`

**Full-stack Developer — Chaos** · 2024–2025
I developed features for Cylindo's 3D content platform.
I applied Clean Architecture to keep the modules loosely coupled and easier to change.
`Node · TypeScript · React · GraphQL · PostgreSQL`

**Full-stack Developer — Onomondo** · 2022–2024
I built internal tools and infrastructure components.
I improved the developer workflows and the CI/CD pipeline, so releases became faster and
more reliable.
`React · TypeScript · Node · Express · PostgreSQL · Docker · Kubernetes`

**Software Engineer — Tame** · 2021–2022
I modernised webinar and event platforms in an agile team.
I replaced legacy code and shipped new features for users.
`React · TypeScript · Node`

**Full-stack Developer — WireDelta** · 2020–2021
I extended a social media platform.
I made the backend data flows faster, which improved the API response times.
`Angular · TypeScript · Sequelize · Node · Redis`

**Software Developer — 2BM** · 2016–2020
I maintained and extended SaaS tools that enterprise customers use to communicate.
I built mobility features for 2BM Mobile WorkOrder.
`JavaScript · XML`

## How I work with AI tools

I write code with an AI pair, and I am strict about it. I do not ship a claim I have not
checked. I run the command instead of trusting my model of what the command would say.
When one of my review findings is wrong, I write the retraction. I include the evidence
that overturned it.

I gave an internal talk on AI-assisted decision making, built on my own reading notes.

## Also

- **Education:** BSc in IT & Network Technology, Technical University of Denmark.
- **Languages:** Romanian, English, Danish.
- **Currently:** Felix Technologies, Copenhagen.

📧 ccs4ndu@gmail.com · 💼 [linkedin.com/in/ccs4ndu](https://www.linkedin.com/in/ccs4ndu/)
