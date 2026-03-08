---
name: airport-pickups-london
description: Book UK airport and cruise port transfers via Airport Pickups London. Get instant fixed-price quotes, validate flights, and create real bookings for all London airports (Heathrow, Gatwick, Stansted, Luton, City), Edinburgh, and cruise ports (Southampton, Dover, Portsmouth). TfL-licensed, 24/7 service.
homepage: https://www.airport-pickups-london.com
metadata:
  clawdbot:
    emoji: "🚖"
---

# Airport Pickups London — Transfer Booking Skill

This skill connects your agent to Airport Pickups London's booking API via MCP, giving it the ability to get transfer quotes, validate flights, and create real bookings.

## What Your Agent Can Do

- **Get instant quotes** for any UK route — airports, cruise ports, addresses, postcodes
- **Validate flight numbers** — auto-detect terminal, airline, arrival time
- **Create real bookings** — confirmed reservations with booking reference and driver tracking link

## Setup

Add the APL MCP server to your OpenClaw config.

First, register at https://mcp.airport-pickups-london.com/a2a/register to get a free API key, then add it:

```json
{
  "mcpServers": {
    "airport-pickups-london": {
      "url": "https://mcp.airport-pickups-london.com/mcp",
      "headers": {
        "x-api-key": "YOUR_API_KEY"
      }
    }
  }
}
```

Registration is instant and free — just provide your name and email.

## Available Tools

### `getTransferQuote`
Get prices for any UK transfer route.

**Example prompts your agent will handle:**
- "How much is a taxi from Heathrow to central London?"
- "Get me a quote from Gatwick to Brighton for 4 passengers"
- "What's the price from Southampton cruise port to London?"

### `validateFlight`
Verify a flight number and get terminal, airline, and arrival time.

**Example prompts:**
- "Check flight BA2534 arriving on April 15th"
- "What terminal does EK007 arrive at?"

### `createTransferBooking`
Create a confirmed transfer booking. Returns booking reference and management link.

**Example prompts:**
- "Book a People Carrier from Heathrow to W1K 1LN for John Smith, phone +447123456789, flight BA2534, April 15th at 3pm"

## Pricing Info

- All prices in GBP (£), per vehicle (not per person)
- Fixed prices — no surge, no hidden charges
- Includes meet & greet, waiting time, parking, tolls
- Free cancellation 12+ hours before pickup

## Vehicle Types

| Car Type | Passengers | Suitcases | From |
|----------|-----------|-----------|------|
| Saloon | Up to 3 | 3 | ~£33 |
| People Carrier | Up to 5 | 5 | ~£45 |
| 8 Seater | Up to 8 | 8 | ~£55 |
| Executive Saloon | Up to 3 | 3 | ~£65 |
| Executive MPV | Up to 7 | 7 | ~£85 |

## Important Rules for Agents

1. **ALWAYS call getTransferQuote before booking** — never guess prices
2. **NEVER call createTransferBooking without user confirmation** — always show the price and get a "yes" first
3. Flight validation is optional and never blocks a booking
4. For airport pickups, recommend collection 45-60 minutes after landing

## Support

- 24/7 Phone: +44 208 688 7744
- WhatsApp: +44 7538 989360
- Website: www.airport-pickups-london.com
- Email: info@aplcars.com

## Ratings

TripAdvisor 4.7/5 | Trustpilot 4.9/5 | Reviews.io 4.9/5
