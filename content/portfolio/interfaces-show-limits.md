+++
title = "Interfaces should explain their own limits"
description = "Show what an automated action can change, what it has done, and how a person can correct it."
image = "images/interface-limits.svg"
image_alt = "A bounded panel shows a proposed change, its status, and a visible return path."
weight = 2
preview = true
url = "/ideas/interfaces-should-show-their-limits/"
+++

**Essay.** An interface earns trust when it shows what a system knows, what it will change, and where a person can intervene.

This matters when software suggests or performs a task. A confident tone does not tell a reader how much to rely on a result. Clear limits do.

## State the scope before action

Describe the object and range of the proposed change. “Rename these twelve files” gives a person something to inspect. “Clean up the folder” hides the scope.

Show the source of a suggestion when that source affects the choice. A date, file name, selected text, or user instruction can explain why the system made a proposal.

Do not make a person infer the boundary from an icon or color. Use short labels next to the action.

## Show progress and outcome

During work, report a state that matches the task. Distinguish “waiting,” “working,” “finished,” and “needs attention.” Do not show a completed state while important work remains.

After work, summarize the result in terms a person can check. If a system changes several items, list the changed items and mark any that it skipped. A useful summary helps someone decide whether to continue.

## Make correction part of the flow

Place a review step before changes that are difficult to reverse. Offer a clear way to cancel, undo, or edit the result when the system can provide one.

A small example makes this concrete: an assistant that proposes file changes could show each name before applying them. It could also offer a preview, report skipped files, and keep a return path beside the result.

If the system cannot undo a change, say so before the action. If it cannot inspect a source, say which source it did not inspect.

## Treat limits as interface content

A limitation is useful only when people can see it at the right time. Put constraints beside the choice they affect. Use words as well as color. Keep uncertainty visible instead of hiding it behind a score.

Trust grows from a person's ability to understand and correct a system. The interface should make that ability part of the task.
