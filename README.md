# Unity Game Line 3 / WIP - Puzzle

Getting Started Game - Proof of Concept

![](gif/Match-Three-v.0.9.1.gif)


# [Video PlayList](https://www.youtube.com/playlist?list=PLNph7ndeSqE8GtUUGKSLgPERU7Lj6-8YI)
* 13 - Match Line 3 - Auto Match 3 Vertical - Fruit legends
* 12 - Match Line 3 - Auto Match 3 Horizontal - Fruit legends
* 11 - Match Line 3 - Animation drop cubes
* 10 - Match Line 3 - Match line-link with new drop cubes
* 09 - Match Line 3 - match with new drop cubes
* 08 - Match Line 3 - Remove line-link cubes w/up touch
* 07 - Match Line 3 - linked cube w/line & point
* 06 - Match Line 3 - linked cube w/line
* 05 - Match Line 3 - Line Draw
* 04 - Match Line 3 - Reset
* 03 - Match Line 3 - Start Dialog
* 02 - Match Line 3 - Mount Board
* 01 - Match Line 3 - Proof of Concept Mobile
* 00 - Match Line 3 - Proof of Concept Desktop

## Life cycle
```c#
```

## Puzzle Core States
```c#
public enum PuzzleState {
	STAND,
	DROP_NODES,
	FIND_MATCH,
	CLEAR_NODES,
	RESET_ON,
	RESET_OFF,
	PAUSE_ON,
	PAUSE_OFF
}

```

## Puzzle Events

### Puzzle State Machine 
```c#
event EventHandler OnDropNodesCurrentState;
event EventHandler OnClearNodesCurrentState;
event EventHandler OnFindMatchAutoLineCurrentState;
event EventHandler OnPauseONMatchCurrentState;
event EventHandler OnPauseOFFMatchCurrentState;
event EventHandler OnResetMatchCurrentState;
event EventHandler OnEndResetMatchCurrentState;
```

### Puzzle Configuration
```c#
event EventHandler OnStartPauseGame;
event EventHandler OnEndPauseGame;
event EventHandler OnNewMatch;
event EventHandler OnInitializeGame;
event EventHandler OnResetMatch;
```

### Puzzle Core Controller
```c#
event EventHandler OnNodeModelMatch;
event EventHandler OnResetNoAutoMatch;
event EventHandler OnNoLinkAutoMatch;
event EventHandler OnStartTouchFirstNodeModel;
event EventHandler OnEndTouchFirstNodeModel;
event EventHandler OnStartMovimentSameNodeModel;
event EventHandler OnEndMovimentSameNodeModel;
event EventHandler OnEndMovimentDifferentNodeModel;
event EventHandler OnStartMovimentDifferentNodeModel;
```

### Puzzle Match Controller
```c#
event EventHandler OnDispose;
```

### Puzzle Animation Node Controller
```c#
event EventHandler OnCompleteAnimation;
event EventHandler OnStartAnimation;
event EventHandler OnDisposeEffectAnimation;
```
