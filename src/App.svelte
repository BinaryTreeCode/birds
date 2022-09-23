<script>
  import { CircleBufferGeometry, MeshStandardMaterial, BoxBufferGeometry, DoubleSide } from 'three'
  import { DEG2RAD } from 'three/src/math/MathUtils'
  import {
    AmbientLight,
    Canvas,
    DirectionalLight,
    Group,
    HemisphereLight,
    Mesh,
    OrbitControls,
    PerspectiveCamera
  } from '@threlte/core'
  import { spring } from 'svelte/motion'
  import { GLTF } from '@threlte/extras'

  const scale = spring(1)
</script>

<div>
  <Canvas shadows={true} size={{width: 500, height: 500 }}>
    <PerspectiveCamera position={{ x: 50, y: 0, z: 0 }} fov={26}>
      <OrbitControls
        maxPolarAngle={DEG2RAD * 80}
        autoRotate={true}
        enableZoom={true}
        target={{ y: 0.5 }}
      />
    </PerspectiveCamera>

    <DirectionalLight shadow position={{ x: 3, y: 10, z: 10 }} />
    <DirectionalLight position={{ x: -3, y: 10, z: -10 }} intensity={0.2} />
    <AmbientLight intensity={0.2} />


    <GLTF castShadow receiveShadow url={'https://raw.githubusercontent.com/BinaryTreeCode/3d/master/conejo.gltf'} position={{ y: -6.3, x: -0.5 }} scale={5} interactive />
  </Canvas>
</div>

<canvas ></canvas>

<style>
  div {
    height: 100%;
    width: 100%;
  }
</style>
