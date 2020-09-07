# Dual Universe HUD

**!!!WORK IN PROGRESS!!!**


**May not work with seats at the moment, use a programming board**


* Paste **hud.lua** code in to `system->start()`
* Paste `system.showScreen(0)` in to `system->stop()`
* Choose between updater 
    1. `system->update()` where hud refreshes every frame
        * Paste `updateHud()` in to `system->update()`
    2. `unit->tick()` where hud refresh rate can be chosen
        * Paste `unit.setTimer("updateHud", 1/x)` in to unit.start(). For example `unit.setTimer("updateHud", 1/30)` has refresh rate of 30 times a second
        * Create `tick(updateHud)` event and paste `updateHud()` in to it
