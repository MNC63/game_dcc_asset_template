# Naming Convention Guidelines  
(Game Asset – Maya → Unreal Engine)

This document defines **clear and consistent naming rules** for creating game assets using **Autodesk Maya** and exporting to **Unreal Engine**.

The goal is to:
- Avoid ambiguity
- Improve readability
- Support scalability
- Match Unreal Engine standards
- Reflect a Technical Artist mindset

---

## 1. General Rules

- Use **English only**
- Use **PascalCase** for asset names
- Use **underscores `_`** to separate semantic blocks
- No spaces
- No special characters (`@ # $ %`)
- Be **explicit**, not clever

✅ Good:
SM_Rifle_AK_LOD0
T_Rifle_AK_Normal

❌ Bad:
rifle-final
My Asset
asset123!!!

---

## 2. Asset Name Structure

Example:
SM_Crate_Wood_LOD0
T_Crate_Wood_BaseColor

---

## 3. Prefix Definitions

### Mesh / Geometry
| Prefix | Meaning |
|------|--------|
| `SM` | Static Mesh |
| `SK` | Skeletal Mesh |

Example:
SM_Barrel_Metal_LOD0

---

### Materials
| Prefix | Meaning |
|------|--------|
| `M` | Material |
| `MI` | Material Instance |

Example:
### Materials
| Prefix | Meaning |
|------|--------|
| `M` | Material |
| `MI` | Material Instance |

Example:
M_Barrel_Metal
MI_Barrel_Metal_Rusty

---

### Textures (Unreal Standard)

| Prefix | Usage |
|------|------|
| `T_` | Texture |

| Suffix | Meaning |
|------|--------|
| `BaseColor` | Albedo |
| `Normal` | Normal map |
| `ORM` | Occlusion / Roughness / Metallic |
| `Emissive` | Emissive |
| `Opacity` | Opacity / Mask |

Example:
T_Barrel_Metal_BaseColor
T_Barrel_Metal_Normal
T_Barrel_Metal_ORM

---

### Rigs & Helpers (if needed)

| Prefix | Meaning |
|------|--------|
| `CTRL` | Control object |
| `JNT` | Joint |
| `LOC` | Locator |
| `GRP` | Group |

Example:
CTRL_Grip
JNT_Trigger
GRP_RIG

---

## 4. Maya File Naming

### Working Files
assetName_v###.ma

Example:
Rifle_AK_v001.ma
Rifle_AK_v010.ma

Rules:
- Always use **3-digit versioning**
- Never overwrite previous versions
- `.ma` preferred for diff & debugging

---

## 5. LOD Naming

### Mesh
SM_<AssetName>LOD0
SM<AssetName>LOD1
SM<AssetName>_LOD2

Example:
SM_Rifle_AK_LOD0
SM_Rifle_AK_LOD1

---

## 6. FBX Export Naming

- **One FBX per asset**
- Export by selection

<AssetName>_LOD0.fbx

Example:
Rifle_AK_LOD0.fbx

---

## 7. Folder Naming

- Lowercase
- No spaces
- Descriptive

Example:
maya/
textures/
reference/

---

## 8. Unreal Engine Compatibility Notes

- Naming follows Epic Games recommendations
- Consistent prefixes improve:
  - Content Browser filtering
  - Automation
  - Tool scripting
- Avoid renaming assets after importing into UE

---

## 9. When to Extend the Convention

You may extend this naming system when:
- Asset becomes animation-heavy
- Asset requires multiple variants
- Team size increases

But:
> **Do not add complexity unless the asset demands it.**

---

## 10. Summary Philosophy

Good naming is:
- Predictable
- Boring
- Scalable

If someone opens the project and understands the asset structure **without asking you**, the naming is correct.

---

