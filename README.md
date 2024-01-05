import matplotlib.pyplot as plt
import matplotlib.patches as patches

# Create a figure and axis
fig, ax = plt.subplots(figsize=(8, 6))

# Legionella representation
legionella = patches.Circle((0.5, 0.5), 0.3, color='red', label='Legionella')

# Nanoparticles (CNT and ION)
cnt = patches.Rectangle((0.2, 0.7), 0.1, 0.1, color='blue', label='CNT')
ion = patches.Rectangle((0.6, 0.7), 0.1, 0.1, color='green', label='ION')

# Arrows indicating development pathways
arrow1 = patches.FancyArrowPatch((0.5, 0.4), (0.3, 0.6), mutation_scale=15, color='black', label='Development Pathway')
arrow2 = patches.FancyArrowPatch((0.5, 0.4), (0.7, 0.6), mutation_scale=15, color='black')

# Additional features (CNT and ION in adsorbents/membranes)
adsorbent = patches.Rectangle((0.2, 0.2), 0.1, 0.1, color='purple', label='Adsorbents/Membranes')

# Annotation
plt.text(0.5, 0.85, 'Nanoparticle-Based Legionella Elimination', ha='center', va='center', fontsize=12)

# Set axis limits and remove ticks
ax.set_xlim(0, 1)
ax.set_ylim(0, 1)
ax.set_xticks([])
ax.set_yticks([])

# Add patches to the axis
ax.add_patch(legionella)
ax.add_patch(cnt)
ax.add_patch(ion)
ax.add_patch(arrow1)
ax.add_patch(arrow2)
ax.add_patch(adsorbent)

# Add legend
ax.legend(loc='upper right', bbox_to_anchor=(1, 1))

# Show the plot
plt.show()
