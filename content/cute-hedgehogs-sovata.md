+++
date = '2025-11-20T18:13:00+02:00'
draft = true
title = 'Cute Hedgehogs in Sovata'
summary = """
Discover the **adorable European hedgehogs** that call Sovata home!

Learn where to spot them, fascinating facts about these *spiny creatures*, and see a Scala implementation for tracking hedgehog sightings.
"""
+++

## Discovering Hedgehogs in Sovata

Sovata, a picturesque spa town in Transylvania, Romania, is famous for its therapeutic salt lakes. But there's another delightful resident that visitors sometimes encounter: the adorable European hedgehog!

### Where to Spot Them

Hedgehogs in Sovata are most active during:
- **Evening hours** - They come out at dusk to forage for food
- **Spring and summer** - Most active during warmer months
- **Garden areas** - Near Bear Lake and around local guesthouses

### Fascinating Hedgehog Facts

1. **Spiny defense** - They have about 5,000-7,000 spines
2. **Insectivores** - They love eating beetles, caterpillars, and slugs
3. **Hibernators** - They sleep through Romanian winters
4. **Ancient creatures** - Hedgehogs have been around for 15 million years!

### Hedgehog Tracking System

If you wanted to track hedgehog sightings in Sovata, here's a simple Scala implementation:

```scala
import java.time.LocalDateTime

case class HedgehogSighting(
  location: String,
  time: LocalDateTime,
  size: String, // "small", "medium", "large"
  behavior: String
) {
  def isNocturnal: Boolean = {
    val hour = time.getHour
    hour >= 20 || hour <= 6
  }
}

object HedgehogTracker extends App {
  val sightings = List(
    HedgehogSighting(
      location = "Bear Lake path",
      time = LocalDateTime.of(2025, 11, 20, 21, 30),
      size = "medium",
      behavior = "foraging near bushes"
    ),
    HedgehogSighting(
      location = "Hotel garden",
      time = LocalDateTime.of(2025, 11, 19, 22, 15),
      size = "small",
      behavior = "drinking from pond"
    )
  )

  sightings.foreach { sighting =>
    val timeIndicator = if (sighting.isNocturnal) "🌙" else "☀️"
    println(s"$timeIndicator Hedgehog spotted at ${sighting.location}")
  }
}
```

### Hedgehog-Friendly Tourism

If you visit Sovata and spot a hedgehog:
- **Don't touch** - They can roll into a ball when scared
- **Give them space** - Observe from a distance
- **No feeding** - They find their own food naturally
- **Watch quietly** - They have excellent hearing

The combination of thermal lakes, forest trails, and friendly hedgehogs makes Sovata a unique destination in Romania!
