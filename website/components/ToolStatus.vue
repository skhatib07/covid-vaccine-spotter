<template>
  <div>
    <h3>Tool Status</h3>
    <div class="table-responsive">
      <table class="table table-bordered">
        <thead>
          <tr class="table-primary-dark">
            <th>Pharmacy</th>
            <th>Scanning</th>
            <th>Last Checked</th>
          </tr>
        </thead>
        <tbody>
          <tool-status-row
            v-for="providerBrand in $store.state.usStates.usState.metadata
              .provider_brands"
            :key="providerBrand.id"
            :provider-brand="providerBrand"
          >
          </tool-status-row>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.table-primary-dark th {
  color: #fff;
  background-color: #0d6efd;
}
</style>
