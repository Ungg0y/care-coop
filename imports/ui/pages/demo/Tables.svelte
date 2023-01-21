<script>
    import Top from "../../include/Top.svelte";
    import Sidebar from "../../nav/Sidebar.svelte";
    import Footer from '../../include/Footer.svelte';
    import TableData from "./graph-tables/TableData.svelte";
</script>
<div class="sb-nav-fixed">
    <Top />
    <div id="layoutSidenav">
      <Sidebar />
      <div id="layoutSidenav_content">
          <main>
            <div class="container-fluid px-4">
                <h1 class="mt-4">Tables</h1>
                <ol class="breadcrumb mb-4">
                    <li class="breadcrumb-item"><a href="#/">Dashboard</a></li>
                    <li class="breadcrumb-item active">Tables</li>
                </ol>
                <div class="card mb-4">
                    <div class="card-body">
                        DataTables is a third party plugin that is used to generate the demo table below. For more information about DataTables, please visit the
                        <a target="blank" href="https://datatables.net/">official DataTables documentation</a>
                        .
                    </div>
                </div>
                <div class="card mb-4">
                    <div class="card-header">
                        <i class="fas fa-table me-1"></i>
                        DataTable Example
                    </div>
                    <div class="card-body">
                        <TableData />
                    </div>
                </div>
            </div>
          </main>
          <Footer />
      </div>
    </div>
  </div>