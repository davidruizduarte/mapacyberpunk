# mapacyberpunk
import matplotlib.pyplot as plt
import networkx as nx
import numpy as np

# Create our NetworkX graph
G = nx.Graph()

# Add Nodes (Districts)
G.add_nodes_from(["The Sprawl", "Tech Zone", "Old Town", "The Docks"])

# Connect nodes with edges
G.add_edge("The Sprawl", "Tech Zone", weight=3)
G.add_edge("Tech Zone", "Old Town", weight=1)
# ... add more connections

# Basic Plotting
plt.figure(figsize=(8,6))
nx.draw(G, with_labels=True, node_color='skyblue', edge_color='gray')
plt.show()

# Create our NetworkX graph
G = nx.Graph()

# Add Nodes (Districts)
G.add_nodes_from(["The Sprawl", "Tech Zone", "Old Town", "The Docks"])

# Connect nodes with edges
G.add_edge("The Sprawl", "Tech Zone", weight=3)
G.add_edge("Tech Zone", "Old Town", weight=1)
# ... add more connections
# Basic Plotting
plt.figure(figsize=(8,6))
nx.draw(G, with_labels=True, node_color='skyblue', edge_color='gray')
plt.show()

import folium

# Sample coordinates (you'll need to replace with your map's points)
coordinates = {
    "The Sprawl": (35.6804, 139.7690),  # Example - Tokyo
    "Tech Zone": (40.7128, -74.0060),  # Example - New York
    "Old Town": (51.5074, -0.1278),    # Example - London
    "The Decks": (47.6062, -122.3321),  # Example - Seattle
}

# Create a basic map centered around general city area
map = folium.Map(location=[45.5231, -122.6765], zoom_start=6)

# Add Markers for Districts
for district, coords in coordinates.items():
    folium.Marker(coords, popup=district).add_to(map)

# Save the map as an HTML file
map.save("cyberpunk_map.html")
