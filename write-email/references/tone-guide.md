# Tone & Phrasing Guide

Practical examples for hitting the right tone — professional with moderate warmth.

## Opening lines

**Customer reported an issue:**
- "Thank you for reaching out about this. I understand the flashing issue you're experiencing can be frustrating, and I'd like to help you get it resolved."
- "Thanks for the detailed description — that helps a lot. Let me walk you through what's likely happening here."

**Customer asked a question:**
- "Great question! The short answer is yes, the reComputer J401 does support JetPack 6.x. Here are the details:"
- "Thanks for asking — this is actually a common question, so I'm happy to clarify."

**Following up:**
- "I wanted to follow up on our previous conversation about the PCIe detection issue. I've looked into this further and have some updates."
- "Just checking in — were you able to try the steps I suggested last time? I'd love to hear if it resolved the issue."

## Explaining solutions

**Direct solution:**
- "The root cause here is that the device tree isn't including the correct overlay for your camera module. You can fix this by..."
- "This error typically occurs when the NVMe drive hasn't been properly initialized before flashing. Here's what I'd recommend:"

**Asking for more info:**
- "To narrow this down, could you share the output of `dmesg | grep -i nvme`? This will help me see whether the drive is being detected at the kernel level."
- "Would you mind letting me know which JetPack version you're currently running? The configuration steps differ slightly between JP5 and JP6."

**Workaround while investigating:**
- "While I continue investigating the root cause, here's a workaround that should unblock you in the meantime:"
- "I've seen this behavior before — it's usually related to the power delivery timing. As an immediate workaround, try..."

## Closing lines

- "Please don't hesitate to let me know if you run into any issues with these steps — I'm happy to help troubleshoot further."
- "If this doesn't resolve the issue, feel free to share the full serial console log and I'll take a closer look."
- "Let me know if you have any other questions. I'm here to help!"
- "Hope this helps! Looking forward to hearing how it goes."

## Phrases to avoid

| Avoid | Use instead |
|-------|-------------|
| "We apologize for the inconvenience" (overused) | "I understand this is frustrating — let me help" |
| "Please be advised that" (stiff) | "Just a heads-up:" or directly state it |
| "Do not hesitate to contact us" (cliché) | "Feel free to reach out if you need more help" |
| "Kindly provide" (overly formal) | "Could you share" or "Would you mind sharing" |
| "As per our conversation" (bureaucratic) | "Following up on our discussion" or just reference the topic directly |
| "We are looking into your issue" (vague) | "I'm currently investigating [specific aspect]. I expect to have an update by [timeframe]" |

## Tone calibration by urgency

**Normal inquiry:** Warm and helpful. Take time to explain thoroughly.
> "Thanks for reaching out! The reComputer J401 uses a custom carrier board design, so the flash process is slightly different from the NVIDIA dev kit. Here's what you need to do:"

**Urgent/production-blocking issue:** More direct, skip small talk, focus on the fix.
> "I understand this is blocking your production timeline. Let me give you the quickest path to resolution:"

**Simple question:** Brief and friendly. Don't over-explain.
> "Yep, the J401 supports both NVMe and eMMC boot. By default it boots from NVMe if both are present. Let me know if you need help configuring it!"
