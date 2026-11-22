> User direction, 2026-11-21: research and strategy only. Do not submit image or video generations. Wait for an explicit instruction to begin production after the strategy is agreed. The earlier firefly submission attempt was rejected by the unlimited concurrency limit; no firefly job was created.

# Current AI video workflow

Updated: 2026-11-22. Research is ongoing; see `research/2026-11-21/STATUS.md` for coverage. This guide supersedes conflicting claims in the historical July notes.

## Objective

Find fast-growing AI video formats across niches, understand why viewers share them, and produce original variations. Test in Higgsfield first using the user's verified unlimited entitlement; make eligible final entries in Dreamina. There is no fixed niche. Views and prize payments are targets, never guaranteed outcomes.

## Before generation

Record platform, selected model and version, generation mode, duration, aspect ratio, resolution, audio setting, reference roles, and the displayed cost. A model catalog's support for unlimited generation does not prove that this account or interface has an unlimited allowance. Do not silently substitute credit spending for the requested unlimited workflow.

Credit units differ between providers. Compare the quoted cost of the same model, duration, resolution and workflow, then record accepted output seconds and retries. A larger monthly credit balance alone does not establish better value; historical pricing screenshots do not establish current entitlements.

Higgsfield and Dreamina are platforms; Seedance is a model family. Their interfaces, reference selectors, editing features, account access and pricing differ. Do not paste an API object or invented reference token into the web prompt and assume it controls settings.

## Prompt construction

1. State the visible event: subject, action, location and payoff.
2. Prepare only the references needed: identity, wardrobe, environment, product, motion or voice. Assign each file its role using the platform's actual reference selector. State what must *not* transfer, such as the neutral background of a character sheet.
3. Describe motion, framing and lighting that the references do not settle. Use an observable camera instruction, such as a slow push toward the face. Keep the number of subjects and simultaneous actions manageable.
4. For a sequence, describe ordered shots with manageable story beats. Seedance 2.0's [official guide, updated November 19](https://ai.byteplus.com/ark/region:ap-southeast-1/docs/seedance-2-0-prompt-guide), warns against strict timestamps. Keep timing targets in the editing plan; use model-specific pacing instructions where supported. Finish precise timing in an editor.
5. Specify dialogue, speaker, performance and allowed sound where needed. A physical trigger can motivate an expression better than a list of abstract emotions.
6. End with the intended final state and the few continuity constraints that matter. Long negative lists and extra cinema terminology are not a substitute for clear staging.

There is no universal best word count. JSON may organize a planning document; it is not a documented private rendering-engine schema. Keep real API parameters separate from prose.

For a motion-reference workflow, record separately what transfers from the preview (path, placement, cuts) and what may change (appearance, acting, effects). The [Blender and advertising audits](research/2026-11-22/AD_WORKFLOW_AUDITS.md) expose conflicting asset labels and movement instructions despite exact-match language. Resolve those contradictions first. A match cut also needs comparable subject screen size, direction, silhouette and horizon; identical camera wording does not establish a match. Keep alternate scene recipes separate from the final assembly.

Choose explicitly between retaining both performance and camera, borrowing only the camera, or retaining performance while changing viewpoint. These are briefing choices, not assumed interface modes. Map performers by starting position and preserve assignments through crossings. If exact timing matters, do not simultaneously ask for new anticipations, delays or choreography. The [Motiondojo audit](research/2026-11-22/JOEY_COLLECTION_AUDIT.md) shows how generic camera, contact and mouth constraints can conflict with a specific example. Decide which constraint has priority before testing; verify audio support and reference syntax in the selected platform workflow.

The Blender fight result broadly follows its preview but differs at matched timestamps, including a rolled source view versus an overhead result at 18 seconds. Review camera phase and framing, not just whether the same broad move appears. The [love-story collection](research/2026-11-22/LOVE_STORY_AUDIT.md) also shows why story-wide constraints need per-shot checking: reference names, scale, costume state and reverse-view screen direction must agree before production. Recurring gestures and sound bridges can connect scenes, but finish their timing against accepted footage.

Check the reference itself against the written constraint: the love-story scale sketch depicts a smaller giant-to-hero ratio than either ratio specified in its prose. Its inline and prompt-linked character sheets also use different face masking. Choose one approved version for each role, and resolve image/text conflicts explicitly. Repeated URLs, edited copies and alternative sketches are not independent demonstrations of a technique.

Maintain a scene-boundary record for appearance, prop ownership, position and pending action. The [reviewed short-drama example](research/2026-11-22/DRAMA_AND_EDITING.md) has glasses reappear at its ending despite the earlier no-glasses state; its supplied clips also differ from written durations. A repeated continuity instruction is a request, not evidence of preservation. Compare accepted footage against the record, then finish pacing in the edit. For an editing revision, identify the accepted speech/order/format to preserve and the specific visual changes requested.

Audit a shared recipe before using its recreation button: check uploaded-reference numbering, repeated or conflicting prompt blocks, duration, framing and scene continuity against the actual selected controls. The [reviewed Kaye guides](research/2026-11-22/KAYE_GUIDES.md) include 16:9 prose linked to 4:3 settings, different written/link durations and a duplicated shot prompt. A public recipe's default link is not an original run record. A proposed cheaper method also needs comparable outputs and retry costs before calling it a saving.

Also check which prompt version the result represents. The [realism guide](research/2026-11-22/REALISM_GUIDE_AUDIT.md) explicitly supplies adapted text-only prompts beside earlier project clips. Its revised instructions address a retained taco and cropped head visible in the older scene. Record original media, original inputs when available, adapted instructions and our proposed changes separately. A difference from a later prompt is not evidence that the model failed that prompt. A placement diagram can also crop a character while the desired shot needs their whole head; specify final framing separately from seating geometry.

A full-looking prompt can still omit the scene. The [301-vote cinematic post](https://www.reddit.com/r/seedance2pro/comments/1xl173h/how_to_create_cinematic_ai_videos_with_seedance/) supplies style preferences but none of its demonstrated chase, obstacles or rescue. Before adopting a recipe, identify where the actual event and geography are specified—in text, reference media or a preset. If that input is absent, record the gap rather than crediting generic quality words with producing the story.

For Seedance 2.0, the same official guide recommends separate face and body references over multi-view character composites, which can cause duplicate subjects. It also distinguishes editing an existing video from borrowing its motion or style. Match the wording to that task; verify the platform's supported mode separately.

A short motion prompt may depend on substantial image preparation. The [reviewed falling montage](https://www.instagram.com/reel/DT2N8DJCIrq/) first creates consistent scene variants, uses two endpoints for its main move and single images for detail shots, then edits the clips together. Record that full setup when learning from a successful short prompt.

A storyboard grid is a planning artifact, not necessarily the final video reference. The [historical car workflow](https://www.reddit.com/r/HiggsfieldAI/comments/1pkvuca/nano_banana_pro_multi_angle_trick/) generates a grid, regenerates individual panels, then uses those images as endpoints. Inspect each isolated image against the approved subject; regeneration is not lossless extraction. At joins, compare actual end/start pose, framing and movement direction as well as appearance. Shared target images alone do not prove smooth motion through an edit. Keep image planning, animation and post-production decisions distinct in the experiment log.

A drawn route can communicate landmark order, but it does not establish exact camera control. The [reviewed FPV example](https://www.reddit.com/r/seedance2pro/comments/1twsuqm/seedance_20_path_control_is_basically_ai/) also supplies a detailed written itinerary; its sketch's independent contribution is unknown. Check route order, prop orientation, required visible body parts and the final contact separately. The sample's opening omits a hand required throughout by its prompt. Treat the sketch as a reference technique to test after authorization, not a verified precision-path feature.

A short preset command can also stand for a larger predefined workflow. The [floating-fall catalog check](research/2026-11-21/INSTAGRAM.md#preset-cross-check) identifies separate character, location and product inputs. Treat the command as recipe selection; do not infer that the words alone describe or control every shot.

Before using a multi-stage prompt pack, compare every stage against one continuity record: subject appearance, left/right accessories, location geometry, source-reference roles and camera position. A reviewed [photorealism pack](https://www.reddit.com/r/Seedance_AI/comments/1wop0ju/full_breakdown_how_i_used_claude_opus_seedance_25/) changes car and wardrobe details between stages despite repeated identity-lock instructions. Resolve contradictions before adding more adjectives. Distinguish a fixed viewpoint with slight handheld sway from an absolutely immobile frame.

Inspect the demonstrated result against that record. The same pack's published video puts a steering wheel before a different character than its assigned driver and includes captions despite their exclusion in the prompt. An edited showcase alone cannot tell us which discrepancies arose during generation or post-production. Check spatial roles as well as faces, and distinguish requested behavior from verified behavior.

Check the tutorial's own chain of evidence as well. The [drama demonstration](https://www.instagram.com/reel/Dfu7JNqhC7J/) switches stories between its planning screen and generation screen. The [hologram lesson](https://www.instagram.com/reel/DcAtwfGCqYx/) shows a reference order that differs from its narration. Neither discrepancy proves the technique cannot work, but both prevent treating the displayed sequence as an exact reproducible recipe. Confirm asset roles from actual bindings rather than copying numbered references mechanically.

When a discovery site supplies a prompt reconstructed from a finished reel, label it as a proposed recreation. Prefer the creator’s visible input when available: the [key-to-car tutorial](https://www.instagram.com/reel/DWcIgpEDcjo/) displays an opening prompt, while its linked third-party analysis supplies a different synthesized recipe.

Treat an assistant's script-retention score and estimated narration clock as planning aids. They do not measure viewer retention or guarantee the duration of a delivered performance. After production is authorized, time shots and captions against the actual audio, then inspect the edited result. A workflow that ends with importing clips into an editor still requires editing and review, even if its promotion describes a one-command process.

For acting, connect a visible trigger or spoken line to a restrained physical response, then describe how blocking and framing support it. The [reviewed mother–daughter scene](https://www.reddit.com/r/Seedance_AI/comments/1vrjlk3/seedance_25_acting_prompt_tutorial_how_i_built_a/) builds tension but develops pronounced facial redness and an exaggerated expression near the climax. Treat subtle reactions as a test target, not a guaranteed prompt fix. Inspect the strongest emotional beat as closely as the opening, and keep dialogue timing separate from automatic transcript timestamps, which can overrun the actual file. The published example does not include its full production inputs.

Compare the published prompt’s event and duration with the actual demonstration before borrowing it. A [classroom example](https://www.reddit.com/r/Seedance_AI/comments/1x6t7ph/an_8second_classroom_drama_made_with_seedance_25/) pairs an eight-second gesture prompt with a roughly thirty-second fight. Missing inputs prevent attributing that result to the displayed text. For multi-character action, inspect close-ups and transitions for transferred wardrobe as well as facial identity: the [rooftop example](https://www.reddit.com/r/Seedance_AI/comments/1x97lk3/seedance_25_anime_fight_prompt_a_fourshot_rooftop/) briefly combines the two characters’ assigned clothing details. These are observed failure cases, not evidence for a universal prompt-length limit.

For relighting a recorded performance, separate appearance from motion. The [public relighting tutorial](https://www.instagram.com/reel/DcuzFYappi6/) first prepares a styled still, then supplies that image alongside the original performance video. Its prompts explicitly restrict what should transfer from the style reference. Treat preservation wording as a review target: compare expressions, movement, objects and framing against the source. The public comment and demonstrated prompt box use different endings, so save the exact version used in any later authorized test.

## Platform adaptation

For a morph followed by a camera move, keep the stages explicit: the [reviewed two-pass workflow](research/2026-11-22/INSTAGRAM_TEXT_AUDIT.md#row-8-elastic-morph-before-camera-movement) first requests a locked viewpoint and readable object transformations, then changes the camera while retaining that sequence. Combining the two instructions would create a different experiment.

For a new camera angle on an existing performance, distinguish a re-photography request from a new performance. Name the source master, desired viewpoint and preserved action/eyeline. Build a comparison sheet at important gestures and object contacts after any authorized test. The [reviewed angle demonstration](https://www.reddit.com/r/Seedance_AI/comments/1wnveqr/seedance_25_videotovideo_workflow_reshoot_the/) shows broad alignment, but does not prove frame-exact timing or establish its full model/provider provenance. Keep the original audio separately when exact timing matters; compare the full moving result before editing angles together.

Specify whether the performer keeps addressing the original camera or looks toward the new viewpoint. The [hybrid tutorial's visible guide](research/2026-11-22/INSTAGRAM_TEXT_AUDIT.md#row-9-preserve-eyeline-when-adding-a-second-camera) explicitly retains the original eyeline, then uses a separate Object Swap pass for wardrobe. A change of viewpoint does not imply a change of gaze or clothing.

For references reused across scenes, record one explicit mapping per asset: subject, permitted attributes, excluded attributes, prop owner and scene of use. Several views of one prop should be labeled as one prop. For extensions, describe the actual accepted boundary pose, prop placement and motion direction. These are planning conventions supported by [supplemental provider guidance](research/2026-11-21/SUPPLEMENTAL_GUIDES.md#atlas-cloud-editing-and-reference-assignment), not guarantees that the model will obey.

| Task | Higgsfield | Dreamina |
| --- | --- | --- |
| Reuse identity | Select saved Elements or attach approved references; Soul ID training is not automatically applied across all models | Attach approved references and assign their roles in the selected model's workflow |
| Iterate | Verify the web unlimited toggle, eligible model/settings and displayed cost | Use available Draft mode or a smaller test; verify current cost |
| Repair | Use the available video-edit workflow with explicit source preservation and the requested change | Use available local/segment editing where appropriate; inspect unaffected regions afterward |
| Finish | Compare final output against the approved draft; re-generation may alter it | Preserve generation provenance and reusable workflow for a potential Spotlight submission |

Live Higgsfield catalog observed on 2026-11-21: Seedance 2.0 offers 4–15 seconds; 2.5 offers 4–30 seconds. The 2.5 catalog lists up to 30 image, 10 video and 10 audio references; these are ceilings, not targets. Some help pages show older resolution limits. Use the actual selected interface's validation before submission. Recheck these facts whenever models change.

The [November 11–12 release notes](https://higgsfield.ai/creator-hub/changelog) now distinguish Seedance 2.5's 4K output from the separate Flash model's 480p/720p previews. The 4K announcement covers standard generation, extension and selected drafts, at 4–30 seconds; bitrate affects detail and cost. Both announcements exclude US availability at observation. These platform announcements do not prove this account's access or unlimited entitlement. Flash, Draft Mode and a lower resolution are distinct choices: record the actual choice, then inspect a new final render against the accepted preview rather than assuming exact preservation.

Keep platform workflow limits separate from model limits. A historical [Dreamina Long Video demonstration](https://www.instagram.com/reel/DbqeDeROWkh/) shows a 180-second duration control, while its example prompt asks for a 30-second commercial. It does not demonstrate a completed three-minute result or establish current account access. Do not transfer that interface's duration or reference-count claims to Higgsfield because both use the Seedance name; align the written target and selected duration before any authorized test.

## Test and review

When transferring a recorded performance into a relit scene, record which input supplies the background as well as which supplies motion. A [reviewed historical walkthrough](research/2026-11-22/INSTAGRAM_TEXT_AUDIT.md) selects Image in Kling 3.0 Motion Control's Scene control setting. Its lighting prompt alone does not capture that setup. Tutorials may also change aspect, resolution or output count between edited screens; capture the final shown controls and verify their current equivalents only when preparing an authorized run.

For complex spatial relationships, consider a numbered storyboard before video generation. In the [reviewed Dreamina demonstration](https://www.instagram.com/reel/De1nVnoBMsp/), simple Blender geometry establishes scale, while panels describe composition and action and separate references define appearance. This trades exact motion-reference copying for more freedom between key poses. Treat improved motion and reduced cost as hypotheses to test; the creator supplied no controlled success rate. Blender is an optional planning tool, not a requirement for every short video, and the full automation prompt was gated.

A blocking diagram can also state the ground level, raised surfaces, relative subject sizes and foreground/background positions. The [reviewed film discussion](https://www.reddit.com/r/Seedance_AI/comments/1w675bp/i_used_seedance_for_most_of_a_12minute_ai_film_a/) supplies concrete examples. Label diagram colors as identity markers rather than desired wardrobe; numerical size annotations express intent, not a guaranteed model setting. Separate a creator's used method from suggestions they explicitly have not tried.

Keep an experiment log: hypothesis, exact prompt, reference versions, settings, cost, output/job ID, observed defect, next change. Compare variants with one controlled change, and repeat promising variants before declaring a rule. A selected showcase video does not establish a success rate.

Record audio post-production as well. A [reviewed historical tutorial](https://www.youtube.com/watch?v=5cdzvOua-_g) separates vocals, enhances speech and adds music before publishing. Its final soundtrack cannot demonstrate the generator's unprocessed voice quality. Preserve raw and finished audio separately for later comparisons.

Watch every generated second, including transitions. Check identity, hands, object permanence, contact, direction of motion, camera intent, audio and the ending. Inspect the exported file's actual duration and dimensions. Upscaling, a new high-resolution generation, and native high-resolution rendering are different operations; none recovers unknown original detail with certainty.

For depth-guided regeneration, inspect what the depth map omits before relying on it. A [reviewed comparison](https://higgsfield.ai/@alpius/blogs/draft-mode-without-draft-mode-finish-your-480p-seedance-take-at-4k) shows thin arrows missing from the depth reference and changed props/crowds in the regenerated crops. Evaluate detail, identity, staging and timing separately. A similarity percentage without a defined metric and alignment method is not a quality score or success rate; a still comparison cannot establish moving continuity. Treat these observations as reasons for later tests, not validated settings for our account.

## Sources

- [Official Seedance prompt guide](https://higgsfield.ai/enterprise-help-center/platform/seedance-prompt-guides): reference roles, staging and approximate timing.
- [Higgsfield model help](https://higgsfield.ai/creator-hub/help-center/ai-models/how-do-i-use-seedance): model workflows and account/interface distinctions.
- [Dreamina Draft workflow](https://dreamina.capcut.com/seedance/seedance-2-5-draft): draft-to-final workflow; check availability and expiry in the account.
- [Teacher's Tech tutorial](https://www.youtube.com/watch?v=AvB-dfxTMgE): full transcript reviewed; sponsored demonstration of beats, staging and reference roles.
- [Kaye workflow](https://www.youtube.com/watch?v=USPWGH5YcIU): full transcript reviewed; character/location/keyframe preparation. Product rankings, prices and absolute consistency claims are creator claims, not adopted as facts.
