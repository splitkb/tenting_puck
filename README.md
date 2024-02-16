# Tenting Puck

The tenting puck is an adapter which allows you to mount any 1/4th inch threaded camera tripod to your keyboard or other device. It's the most common threading used on just about any camera tripod, which greatly increases the versatility of your setup!

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## How do I use these files?

First off, if your keyboard already supports the tenting puck, you can just go ahead and use the puck! It mounts directly to the PCB using four 4mm M2 screws.

Most keyboards sold by splitkb.com support the puck, like the Kyria and all kits in the Aurora Series.

If you're making your own keyboard, then you can do either one of the following:

1. **Add support for the tenting puck to your keyboard.** You can do this by using the `TentingPuck.kicad_mod` or `TentingPuck_NoHole.kicad_mod` file in Kicad. This is a footprint file, which you can assign to a symbol in the schematics editor and then add to your keyboard's PCB.
2. **Drill holes in a bottom plate.** Print the `puck_drill_template.pdf` at 100% scale, tape it to your plate and then drill the holes using a 2.5mm diameter drill (anything between 2.3 and 2.8mm will work, so drill sizes 43 to 35).

## Which footprint do I need?

- Use `TentingPuck.kicad_mod` if your PCB has enough space to allow for it.
- Otherwise, use `TentingPuck_NoHole.kicad_mod`.

## Dimensions

- Puck diameter: 41.1mm
- Puck total height: 6.6mm
- Puck screw post dimensions: 3 x 3mm
- Puck screw post thread depth: _up to_ 5.6mm
  - Manufacturing the threading is challenging, and so the thread depth will vary between individual holes. I recommend using up to 3mm of the thread depth, so we include 4mm M2 screws, which go through 1.6mm of PCB to then use a remaining 2.4mm of threading.
- Clearance between PCB and puck body: 2.4mm

All dimensions should be within a tolerance of ±0.1mm.

## Important design notes

- Adding puck support to a split keyboard? It helps to place the puck at the exact same coordinate (based on its center), so you can use identical bottom plates if your keyboard is symmetrical.
- Keep the puck dimensions in mind when designing - don't place tall components below the puck, and keep the puck screw posts clear from parts like hotswap sockets and pads.
- The puck may be conductive. If you're adding a shield net to your keyboard, it can help to ground the puck through that.
- Keep tolerances in mind: keep a small bit of space around the puck and its posts, so you have a little leeway during assembly.
- The center hole may be omitted, most tripods do not have a long enough thread length to use the extra clearance.
- You may omit screw holes if they don't fit, but do mind that the puck may be conductive and you do need to keep the bottom of the PCB free of any pads or components where the screw post touches.
